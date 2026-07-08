# Design Spec: Scarcity Section

## Overview
A section explaining the value of limited editions. Uses a subtle background accent to highlight the importance of the message and build perceived value through scarcity.

## Architecture
- **Layout:** Centered content with a distinct background (`bg-primary/5`).
- **Spacing:** `py-20`, `px-6`.
- **Typography:**
    - Heading: `text-3xl md:text-4xl font-bold tracking-tight text-foreground`
    - Body: `text-lg text-muted-foreground mt-8 leading-relaxed max-w-xl mx-auto`
- **Visuals:** Minimalist iconography (e.g., Lucide `Award` or `Gem`) to denote exclusivity.

## Implementation Steps
1. Create `src/lib/scarcity-content.ts` for text content.
2. Add Scarcity section to `src/pages/index.astro`.
3. Ensure responsive padding/margins and mobile-first readability.
