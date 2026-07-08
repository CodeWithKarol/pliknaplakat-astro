# Collections Section Implementation Plan

> **For agentic workers:** REQUIRED: Use superpowers:executing-plans to implement this plan. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Implement the Collections section in `src/pages/index.astro`.

**Architecture:** Use a data-driven approach to populate a responsive grid of product collection cards.

**Tech Stack:** Astro, Tailwind CSS (v4), shadcn/ui.

---

## Chunk 1: Implementation

### Task 1: Update `src/pages/index.astro`

**Files:**
- Create: `src/lib/collections-content.ts`
- Modify: `src/pages/index.astro`

- [ ] **Step 1: Create `src/lib/collections-content.ts`**

```typescript
export const collections = [
  {
    title: "Włoskie Lato",
    description: "Idealne do salonu. Ciepłe światło, wakacyjny luz.",
    price: "49 zł"
  },
  {
    title: "Skandynawski Minimalizm",
    description: "Czysta forma do sypialni lub biura. Chłodne, kojące barwy.",
    price: "49 zł"
  },
  {
    title: "Miejski Detal",
    description: "Artystyczne zbliżenia architektury. Nowoczesny sznyt w czerni i bieli.",
    price: "49 zł"
  }
]
```

- [ ] **Step 2: Add Collections section to `src/pages/index.astro`**

```astro
---
import { collections } from "@/lib/collections-content"
// ...
---

<!-- ... Storytelling Section ... -->

<!-- Collections Section -->
<section class="max-w-7xl mx-auto px-6 py-24">
  <div class="text-center">
    <h2 class="text-3xl md:text-4xl font-bold tracking-tight text-foreground">
      Gotowe zestawy, które odmienią Twój dom.
    </h2>
    <p class="max-w-xl mx-auto text-center mt-4 text-lg text-muted-foreground">
      Nie musisz być projektantem, by mieć wnętrze z charakterem. Wybrałem dla Ciebie najlepsze kadry z moich podróży i pogrupowałem je w zestawy.
    </p>
  </div>
  
  <div class="grid md:grid-cols-3 gap-8 mt-16">
    {collections.map((item) => (
      <div class="group">
        <div class="aspect-[3/4] bg-muted rounded-xl mb-6 shadow-md transition-transform group-hover:scale-[1.02]"></div>
        <h3 class="text-xl font-semibold">{item.title}</h3>
        <p class="text-sm text-muted-foreground mt-2">{item.description}</p>
        <p class="text-lg font-bold mt-4 text-primary">{item.price}</p>
        <Button variant="outline" className="mt-4 w-full">Wybierz zestaw</Button>
      </div>
    ))}
  </div>
</section>
```

- [ ] **Step 3: Commit**

```bash
git add src/pages/index.astro src/lib/collections-content.ts
git commit -m "feat: implement collections section"
```

## Chunk 2: Verification

### Task 2: Verify Standards

- [ ] **Step 1: Run build and lint**

Run: `npm run lint && npm run typecheck && npm run build`
Expected: PASS

- [ ] **Step 2: Final commit**

```bash
git commit -am "chore: verify collections implementation"
```
