# Design Spec: Footer (MVP)

## Overview
A clean, trust-focused footer acting as the final conversion point and authority marker.

## Architecture
- **Layout:** Responsive grid (1 col mobile, 3 cols desktop).
- **Spacing:** `py-16`, `px-6`, `bg-muted/30`.
- **Columns:**
    1. **Identity:** Brand name/slogan.
    2. **Offer:** Links to 3 collections + guide.
    3. **Trust:** Contact email, legal links.
- **Copyright:** Small text at the bottom.

## Implementation Steps
1. Create `src/components/Footer.astro`.
2. Integrate footer into `src/layouts/main.astro`.
3. Verify mobile-first layout and alignment.
