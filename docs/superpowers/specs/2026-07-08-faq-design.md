# Design Spec: FAQ Section (SEO-friendly)

## Overview
A simple, SEO-optimized FAQ section to resolve final purchase objections and rank for common questions.

## Architecture
- **Layout:** Centered content column (`max-w-3xl`).
- **Spacing:** `py-24`, `px-6`, `space-y-10` for distinct question blocks.
- **Typography:**
  - Heading: `text-3xl font-bold`
  - Questions (H3): `text-lg font-semibold`
  - Answers: `text-muted-foreground mt-2`

## Implementation Steps
1. Create `src/lib/faq-content.ts` for structured text content.
2. Implement FAQ section in `src/pages/index.astro`.
3. Verify mobile-first layout.
