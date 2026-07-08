# Design Spec: Education/Guide Section

## Overview
A value-first education section that offers a free guide to solve customer printing concerns. Using icons/cards for readability increases engagement and perceived value.

## Architecture
- **Layout:** Centered heading with a 3-column responsive card layout (`grid sm:grid-cols-3`) for guide points.
- **Spacing:** `py-24`, `px-6`.
- **Card Design:** `bg-card`, `border`, `rounded-xl`, `p-6` for focus.
- **Typography:**
    - Heading: `text-3xl md:text-4xl font-bold`
    - Body: `text-base text-muted-foreground mt-4`
- **Call to Action:** `Button` size `lg` for the free guide download.

## Implementation Steps
1. Create `src/lib/education-content.ts` for text content.
2. Implement Education section in `src/pages/index.astro`.
3. Verify build and responsive styling.
