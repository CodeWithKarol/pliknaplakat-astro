# Scarcity Section Implementation Plan

> **For agentic workers:** REQUIRED: Use superpowers:executing-plans to implement this plan. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Implement the "Scarcity/Limited Edition" section in `src/pages/index.astro`.

**Architecture:** Use a distinct background color section with a central, focused message and minimalist iconography.

**Tech Stack:** Astro, Tailwind CSS (v4), Lucide React (for icons).

---

## Chunk 1: Implementation

### Task 1: Update `src/pages/index.astro`

**Files:**
- Create: `src/lib/scarcity-content.ts`
- Modify: `src/pages/index.astro`

- [ ] **Step 1: Create `src/lib/scarcity-content.ts`**

```typescript
export const scarcityContent = {
  heading: "Dlaczego moje plakaty są limitowane?",
  body: "Większość sprzedawców chce sprzedać ten sam wzór milionowi osób. Ja wierzę, że dekoracja Twojego domu powinna mieć swój charakter. Dlatego każda z moich kolekcji posiada limitowaną liczbę kopii (np. tylko 100 pobrań). Gdy limit zostaje wyczerpany, dany wzór znika z oferty lub przechodzi do archiwum. Kupując u mnie, nie kupujesz zwykłego pliku – inwestujesz w unikalność, która nie jest dostępna dla każdego."
}
```

- [ ] **Step 2: Add Scarcity section to `src/pages/index.astro`**

```astro
---
import { LucideGem } from "lucide-react" // Ensure lucide-react is installed, or use simple SVG
import { scarcityContent } from "@/lib/scarcity-content"
// ... existing imports
---

<!-- ... Collections Section ... -->

<!-- Scarcity Section -->
<section class="bg-primary/5 py-20 px-6">
  <div class="max-w-4xl mx-auto text-center">
    <div class="inline-flex items-center justify-center p-3 rounded-full bg-primary/10 text-primary mb-6">
      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-gem"><path d="M6 3h12l4 6-10 13-10-13Z"/><path d="M11 3 8 9l4 13 4-13-3-6"/><path d="M2 9h20"/></svg>
    </div>
    <h2 class="text-3xl md:text-4xl font-bold tracking-tight text-foreground">
      {scarcityContent.heading}
    </h2>
    <p class="max-w-xl mx-auto text-lg text-muted-foreground mt-8 leading-relaxed">
      {scarcityContent.body}
    </p>
  </div>
</section>
```

- [ ] **Step 3: Commit**

```bash
git add src/pages/index.astro src/lib/scarcity-content.ts
git commit -m "feat: implement scarcity section"
```

## Chunk 2: Verification

### Task 2: Verify Standards

- [ ] **Step 1: Run build and lint**

Run: `npm run lint && npm run typecheck && npm run build`
Expected: PASS

- [ ] **Step 2: Final commit**

```bash
git commit -am "chore: verify scarcity implementation"
```
