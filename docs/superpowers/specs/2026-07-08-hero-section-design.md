# Design Spec: Hero Section

## Overview
A two-column Hero section designed for a premium poster shop. It emphasizes clean typography, whitespace, and a high-quality visual anchor to build trust and convey quality immediately.

## Architecture
- **Responsive Layout:** Grid layout (1 col mobile, 2 cols tablet+) using `md:grid-cols-2`.
- **Spacing:** `py-20`, `gap-12`.
- **Typography:** 
    - Heading (H1): `text-4xl md:text-5xl font-bold tracking-tight`
    - Subtitle: `text-lg text-muted-foreground mt-4`
- **Call to Action:** Primary `Button` for main drop, secondary link for sample download.
- **Visual:** Poster placeholder with `aspect-[3/4]`, `rounded-2xl`, and `shadow-2xl`.

## Component Structure
- `src/pages/index.astro`: Entrypoint containing the layout.
- `src/components/ui/button.tsx`: Existing shadcn/ui button component used for CTA.

## Implementation Steps
1. Create Hero section markup in `src/pages/index.astro`.
2. Style with Tailwind CSS v4.
3. Verify and test responsiveness.
