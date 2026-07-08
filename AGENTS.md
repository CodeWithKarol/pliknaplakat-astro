# AGENTS.md

Compact instructions for OpenCode to maintain high-quality context and efficiency.

## Core Commands
- **Dev:** `npm run dev`
- **Build:** `npm run build`
- **Preview:** `npm run preview`
- **Lint:** `npm run lint`
- **Typecheck:** `npm run typecheck`
- **Format:** `npm run format`

## Architecture & Conventions
- **Framework:** Astro 7 + React 19 + TypeScript.
- **Styling:** Tailwind CSS (v4) with shadcn/ui.
- **Component Imports:** Use path aliases (e.g., `@/components/ui/button`).
- **Shadcn:** Components are generated under `src/components/ui`. Use `npx shadcn@latest add <component>` to add new ones.
- **Structure:**
  - `src/pages/`: Astro entrypoints / routing.
  - `src/components/`: Shared UI components.
  - `src/layouts/`: Common page wrappers.
  - `src/lib/`: Utilities.
  - `src/styles/`: Global styles (tailwind).

## Verification Workflow
Always run in this order for PR-ready quality:
1. `npm run lint`
2. `npm run typecheck`
3. `npm run format` (if needed)
