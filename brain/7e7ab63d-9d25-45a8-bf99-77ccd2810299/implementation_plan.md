# Los Romeros Ltd - Brand Command Center

This plan outlines the creation of a premium single-file HTML landing page for the Los Romeros Limited "Brand Command Center" and deployment to a new GitHub repository.

## User Review Required

> [!WARNING]
> **Design Strategy Collision:** Your request asks to use a "super modern, Silicon Valley, AI" design system with "glassmorphism," "micro-animations," and "distinctive fonts (NOT Inter)". However, it also strictly requires adherence to the **Los Romeros Style Guide**, which dictates "Forensic Minimalism," "rigid borders," "fast linear transitions," and explicitly calls for the **Inter** typeface as the secondary body font alongside Playfair Display.
> 
> **My Proposed Compromise:** I will create a highly elevated **"Corporate Cyber"** aesthetic. 
> - I will adhere strictly to your brand dark mode palette (`Slate-900 background` and `Slate-50 text`).
> - I will keep **Playfair Display** as the authoritative heading font but upgrade the body font from Inter to something slightly more distinctive but still legible and formal, like **Space Grotesk** or **DM Sans** (per the ui-ux-pro-max output).
> - I will employ premium glassmorphism (`backdrop-blur` in Tailwind) and micro-interactions (smooth 300ms transitions) while keeping the *shapes* rigid/minimalist (no pill buttons, only sharp borders) to satisfy the "Forensic" requirement.
> 
> **Please let me know if this hybrid approach is approved or if you want strict adherence to one over the other!**

## Proposed Changes

### 1. Landing Page Assembly
#### [NEW] `c:\ANTIGRAVITY PROJECTS\VELYON - LEGAL COMMAND CENTER\docs\Los_Romeros-Brand_Command_Centre.html`
- **Architecture**: A single-file HTML document bundling all required styles, logic, and assets.
- **Frameworks**: 
  - Tailwind CSS via CDN for styling.
  - Alpine.js (optional) for minor interactivity.
  - Lucide Icons (SVG) mapped via CDN or inline SVGs.
- **Content Map**:
  - **Nav**: Clean sticky navbar offering links to: `Brand Guidelines`, `Brand Kit`, and `Style Guide`.
  - **Hero Section**: Utilizing the generated `Los_Romeros_Logo_Dark.png` with premium text presentation for "Brand Command Center", built from `21st.dev` components.
  - **3 Core Menu Sections**: Large glassmorphic bento-grid tracking cards linking to the guidelines, kit, and styles. Each card will use an AI-generated image (using `generate_image`) matching the dark, forensic motif.
- **Styling Specs**: Dark mode default (`bg-slate-900`). Smooth hover scaling. Clean geometric bounding boxes per brand guidelines.

### 2. GitHub Deployment
- Retrieve an authorization / init for the GitHub repository.
- Use `mcp_github_create_repository` to create `LosRomeros-BrandCommand`.
- Take the final `.html` output and commit it to the `main` branch under `/docs/index.html` (or root `index.html`).
- This will prepare the repo to be hosted via GitHub Pages.

## Open Questions

1. Do you want me to spin up a completely new GitHub repository on your connected GitHub account for this landing page, or is there an existing repository for VELYON that I should merge this into?
2. Are you comfortable with me substituting "Inter" for "DM Sans" to satisfy the "NOT Inter" request while retaining readability?

## Verification Plan

### Automated/Tool Verification
- Verify the single-file structure and valid Tailwind syntax payload.
- Confirm Github MCP action output reports a successfully created repository.

### Manual Verification
- Visual inspection of the file locally (I will ask you to open the HTML file in your browser to verify the aesthetic).
