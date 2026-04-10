# Goal
Develop a premium, single-file HTML landing page named "VELYON - BRAND COMMAND CENTER" that integrates the Velyon Brand Kit, Style Guide, and Brand Guidelines into three distinct menu sections. The page will utilize a bold, dark-mode, glassmorphic aesthetic combined with AI-generated visual assets, and be deployed automatically to a new public GitHub repository.

## Proposed Changes

### Research & Synthesis
Combining the two directives:
1. **Velyon Design System:** Deep Obsidian (`#0A0A0A`), Graphite (`#171717`), Electric Azure (`#3B82F6`), ROI Gold (`#EAB308`).
2. **UI-UX-Pro-Max Output:** Space Grotesk (headings), fluid glassmorphic effects, bento grid showcases.
*Note: Although the script output suggested Brutalism/Pink, we will override that with the core requirement of "Dark mode premium aesthetic with glassmorphism and depth" to align with Velyon's executive identity.*

### Visual Assets Generation
We will use the `generate_image` tool to craft custom, photorealistic assets (e.g., highly technical AI architectures, abstract digital data representations, executive strategic moments) for the Hero and other key sections. The Velyon logo will be embedded where appropriate.

### Component Structure (`Velyon_Brand_Command_Center.html`)
The landing page will be a self-contained HTML file featuring:
- **Tailwind CSS (via CDN)** loaded for styling.
- **Space Grotesk & Plus Jakarta Sans** loaded via Google Fonts.
- **Hero Section:** Magic component layout, super modern entrance with typing effects or shimmering data representations.
- **Navigation Menu:** Sticky, glassmorphic tab navigation linking to three main structural sections:
    1. **Brand Guidelines** 
    2. **Brand Kit** (Colors, Typos, Logos)
    3. **Style Guide** (UI Tokens, Patterns)
- **Bento Grid Layouts:** We will present the color palettes and UI components using a Bento grid card style with hover animations (`scale-105`, glow effects).
- **Lucide Icons (SVG):** Inline SVGs for all iconography, ensuring no emoji usage.

### GitHub Integration
We will utilize the GitHub MCP to:
1. Create a new public repository: `VELYON-BRAND-COMMAND-CENTER`
2. Push `index.html` to the repository.
3. Guide the user to enable GitHub Pages (note: Pages must be flipped on manually in repo settings, though the repo will be ready).

> [!WARNING]
> Since the GitHub MCP cannot explicitly toggle the "Enable GitHub Pages" setting inside repository settings (this requires a REST API call with specific admin tokens not always exposed via the standard tool or manual user intervention), I will push the code successfully to the `main` branch. You will need to click exactly one button in your GitHub Repo Settings -> Pages -> Deploy from a branch -> `main`.

## Verification Plan

### Automated/Manual Testing
- I will verify the Single-file format (no external CSS/JS files).
- I will verify the dark mode color contrast.
- I will verify responsiveness by simulating breakpoints (375px, 768px, 1024px).
- I will verify smooth transitions on hover states.
- I will ensure images generated are cleanly integrated into the HTML as data-URIs or public links.
