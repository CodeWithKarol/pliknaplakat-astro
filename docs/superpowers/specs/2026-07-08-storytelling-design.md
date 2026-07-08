# Design Spec: Storytelling Section

## Overview
A minimalist, high-focus Storytelling section designed to build authority and personal connection. It uses narrow typography and clean whitespace to encourage deep reading.

## Architecture
- **Layout:** Centered, narrow content column (`max-w-2xl`) for focused readability.
- **Spacing:** `py-24`, `px-6`.
- **Typography:** 
    - Heading (H2): `text-3xl md:text-4xl font-bold tracking-tight text-foreground`
    - Body Text: `text-lg text-muted-foreground mt-8 leading-relaxed`
- **Visual Accent:** A left border (`border-l-4 border-primary`) to emphasize the narrative tone.

## Implementation Steps
1. Add Storytelling section to `src/pages/index.astro` below the Hero section.
2. Ensure clean separation from the Hero image background.
3. Verify responsive readability.
