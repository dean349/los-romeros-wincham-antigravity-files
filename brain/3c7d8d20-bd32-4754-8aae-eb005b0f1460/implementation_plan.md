# VELYON - Legal Command Center
## System Architecture & Database Schema

This document outlines the foundational System Architecture and Database Schema for the VELYON Legal Command Center. It adheres to the mandated technical stack (Next.js App Router, Supabase, Vercel AI SDK, strict RLS, and pgvector for RAG).

> [!IMPORTANT]
> **User Review Required**  
> Please review the proposed architecture and PostgreSQL schema logic. Once approved, we will begin scaffolding the Next.js application, initializing Supabase, and mapping out the required API endpoints and edge functions.

---

## 1. System Architecture (The "Engine Room")

### Tech Stack Overview
- **Frontend / Client Layer:** Next.js (App Router), TypeScript, Tailwind CSS, and shadcn/ui components for a premium "Dark Mode" enterprise aesthetic.
- **Backend / Auth / Storage:** Supabase (PostgreSQL database, Supabase Auth with TOTP/2FA, Supabase Storage for AES-256 encrypted document housing).
- **Serverless Compute:** Supabase Edge Functions for secure backend logic (e.g., handling document ingestion, converting to embeddings, LLM orchestration).
- **AI / RAG Pipeline:** Vercel AI SDK communicating with Gemini 1.5 Pro or Claude 3.5 Sonnet, retrieving vector representations stored via `pgvector` in PostgreSQL.
- **Hosting / CI/CD:** Vercel for the Next.js frontend, integrated with GitHub for instant continuous deployment.

### High-Level Request Flow
1. **[User Authentication]:** User logs in via Supabase Auth. Requires MFA (TOTP). Session tokens strictly determine RLS access.
2. **[Document Upload]:** User uploads a legal document to a specific "Virtual Data Room" (Workspace). Document is encrypted and stored in Supabase Storage.
3. **[Vectorization / Ingestion]:** An Edge Function triggers upon upload, chunking the document and generating embeddings via an LLM. Embeddings are stored in the `document_chunks` table using `pgvector`.
4. **[AI Query]:** User asks a question in the chat interface. The Vercel AI SDK sends the query to an Edge Function.
5. **[Context Retrieval]:** Edge Function converts user query to an embedding, does a similarity search (using a Postgres RPC function on `document_chunks`), retrieves grounded context, and streams the completion back from the LLM.

---

## 2. Database Schema & RLS Policies

The core design prioritizes "Strict Bounding" ensuring users only have access to documents and AI vectors within their authorized Virtual Data Rooms (VDRs).

### Core Tables

#### `profiles`
Manages extended user information not handled by default Supabase Auth.
- `id` (uuid, references auth.users)
- `first_name` (text)
- `last_name` (text)
- `role` (enum: 'superadmin', 'lead_counsel', 'compliance_officer', 'client')
- `created_at` (timestamp)

#### `vdrs` (Virtual Data Rooms / Workspaces)
Defines secure, isolated spaces for specific clients or cases.
- `id` (uuid, pk)
- `name` (text)
- `description` (text)
- `created_at` (timestamp)
- `created_by` (uuid, references profiles)

#### `vdr_members`
Junction table determining which users have access to which VDRs, enabling multi-tenancy.
- `vdr_id` (uuid, references vdrs)
- `user_id` (uuid, references profiles)
- `access_level` (enum: 'admin', 'editor', 'viewer')
- `created_at` (timestamp)
- `PRIMARY KEY (vdr_id, user_id)`

#### `documents`
Metadata for uploaded case files and legal documents.
- `id` (uuid, pk)
- `vdr_id` (uuid, references vdrs)
- `uploaded_by` (uuid, references profiles)
- `filename` (text)
- `file_path` (text) -- path in Supabase Storage
- `file_type` (text)
- `encryption_status` (boolean)
- `created_at` (timestamp)

#### `document_chunks` (The pgvector RAG store)
Houses the text chunks and their vectorized embeddings for AI similarity search.
- `id` (uuid, pk)
- `document_id` (uuid, references documents)
- `vdr_id` (uuid, references vdrs) -- Denormalized for extremely strict/fast RLS enforcement
- `content` (text) -- The chunked text
- `embedding` (vector(1536)) -- Dimensions depending on the chosen embedding model
- `created_at` (timestamp)

### Bank-Grade Row Level Security (RLS) Example

Row level security guarantees data isolation at the Postgres level regardless of API flaws.

```sql
-- Enable RLS on vdrs
ALTER TABLE vdrs ENABLE ROW LEVEL SECURITY;

-- Users can only view VDRs they are members of
CREATE POLICY "Users can view assigned VDRs" ON vdrs
FOR SELECT USING (
  EXISTS (
    SELECT 1 FROM vdr_members 
    WHERE vdr_members.vdr_id = vdrs.id 
    AND vdr_members.user_id = auth.uid()
  )
);

-- Enable RLS on documents
ALTER TABLE documents ENABLE ROW LEVEL SECURITY;

-- Users can only SELECT documents if they are in the same VDR
CREATE POLICY "Users can access documents in their VDRs" ON documents
FOR SELECT USING (
  EXISTS (
    SELECT 1 FROM vdr_members 
    WHERE vdr_members.vdr_id = documents.vdr_id 
    AND vdr_members.user_id = auth.uid()
  )
);

-- Enable RLS on AI Vectors (Strict Bounding)
ALTER TABLE document_chunks ENABLE ROW LEVEL SECURITY;

CREATE POLICY "Strict Bounding: Users can only query vectors in their VDRs" ON document_chunks
FOR SELECT USING (
  EXISTS (
    SELECT 1 FROM vdr_members 
    WHERE vdr_members.vdr_id = document_chunks.vdr_id 
    AND vdr_members.user_id = auth.uid()
  )
);
```

---

## 3. UI/UX Design System Guidelines

- **Appearance:** A dark-mode first design using deep grays, rich blacks, and highly legible off-white typography, fitting for premium legaltech software. Brand accents will follow Velyon's style.
- **Component Strategy:** `shadcn/ui` provides unstyled components. We apply customized Tailwind classes to build standard Data Tables (for cases/documents), Cards (for VDR overviews), and Modals/Dialogs.
- **Routing:** Built with Next.js App Router for concurrent rendering and layout persistence. Example paths:
  - `/dashboard`
  - `/vdrs/[vdrId]`
  - `/vdrs/[vdrId]/documents`
  - `/vdrs/[vdrId]/ai-assistant`

## Open Questions
> [!WARNING]  
> 1. Do you have a preferred embedding model in mind (e.g., `text-embedding-3-small`, Google Gecko, etc.)? This will determine the dimension size of the `vector` type in the database.
> 2. Are there specific frontend branding colors we should pull from the Velyon Logo to establish the Tailwind CSS theme variables right away?

## Verification Plan

Because we are creating a foundational spec and architecture, the primary verification step relies on human sign-off:

### Manual Verification
1. Does this architecture and schema accurately capture the capabilities expected in the Discovery & Strategy phase? 
2. Are the security boundaries tight enough to satisfy the "Bank-grade" compliance requirement?
