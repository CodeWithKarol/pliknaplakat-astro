# Design Spec: CTA Section (Dual Action)

## Overview
A secondary CTA section positioned after the Storytelling content, featuring a clear split between primary conversion (collection) and lead generation (sample).

## Architecture
- **Layout:** Centered content with distinct visual weight for each button.
- **Container:** `bg-muted/50`, `py-20`, `px-6`.
- **Typography:**
  - Heading: `text-3xl md:text-4xl font-bold`
  - Action buttons: Primary `Button` for collection, `outline` variant for sample.
- **Responsiveness:** Stacked on mobile (`flex-col`), side-by-side on desktop (`md:flex-row`).

## Implementation Steps
1. Create CTA content in a new file `src/lib/cta-content.ts` for configurability.
2. Add CTA section markup to `src/pages/index.astro`.
3. Verify button alignment, spacing, and mobile responsiveness.
