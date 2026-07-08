# Design Spec: Hero Section (Minimalist)

## Overview
A minimalist, centered Hero section designed for a premium poster shop. Focuses entirely on the value proposition, using typography and whitespace to create an elegant, high-end feel.

## Architecture
- **Layout:** Centered content with `max-w-3xl` for optimal reading width.
- **Spacing:** `py-24`, `px-6`.
- **Typography:** 
    - Heading (H1): `text-5xl md:text-6xl font-bold leading-tight tracking-tight`
    - Subtitle: `text-xl text-muted-foreground mt-6 leading-relaxed`
- **Call to Action:** Centered `Button` + optional secondary link below, using `flex-col sm:flex-row justify-center gap-4`.

## Implementation Steps
1. Update `src/pages/index.astro` to re-center and resize the Hero content.
2. Verify visual balance and responsive spacing.
