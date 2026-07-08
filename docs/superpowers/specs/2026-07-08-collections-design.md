# Design Spec: Collections Section (3-Pillar)

## Overview
A high-conversion collections section showcasing three curated sets of posters. Uses product stacking to minimize purchase friction and increase transaction value.

## Architecture
- **Layout:** Three-column responsive grid (`md:grid-cols-3`).
- **Spacing:** `max-w-7xl`, `gap-8`, `py-24`.
- **Card Design:** 
    - Image Area: `aspect-[3/4]`, `rounded-xl`, `bg-muted` (for mockups).
    - Typography: Title (`text-xl font-semibold`), Description (`text-sm`), Price (`text-lg font-bold`).
- **Call to Action:** `outline` variant `Button` on each card.

## Implementation Steps
1. Create `src/lib/collections-content.ts` for data configuration.
2. Implement Collections section in `src/pages/index.astro`.
3. Verify mobile-first grid behavior and visual consistency.
