# Hero Section Implementation Plan

> **For agentic workers:** REQUIRED: Use superpowers:executing-plans to implement this plan. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Implement the Hero section in `src/pages/index.astro` according to the design specification.

**Architecture:** Use an Astro component wrapper with Tailwind v4 utility classes.

**Tech Stack:** Astro, Tailwind CSS (v4), shadcn/ui.

---

## Chunk 1: Implementation

### Task 1: Update `src/pages/index.astro`

**Files:**
- Modify: `src/pages/index.astro`

- [ ] **Step 1: Replace existing content with Hero layout**

```astro
---
import Layout from "@/layouts/main.astro"
import { Button } from "@/components/ui/button"
---

<Layout>
  <div class="max-w-7xl mx-auto px-6 py-20">
    <div class="grid md:grid-cols-2 gap-12 items-center">
      <div>
        <h1 class="text-4xl md:text-5xl font-bold tracking-tight text-foreground">
          Poczuj autentyczny klimat Europy. Kolekcjonerskie plakaty do druku w jakości galerii sztuki.
        </h1>
        <p class="text-lg text-muted-foreground mt-4 leading-relaxed">
          Zapomnij o masowych dekoracjach z sieciówek. Pobierz wysokiej rozdzielczości zdjęcia z moich podróży – gotowe do wydruku w Twoim domu. Limitowane edycje, które ożywiają wnętrza.
        </p>
        <div class="flex gap-4 mt-8 items-center">
          <Button size="lg">Zobacz najnowszy drop</Button>
          <a href="#" class="text-sm font-medium text-muted-foreground hover:text-foreground transition-colors">
            Pobierz darmowy sampl
          </a>
        </div>
      </div>
      <div class="aspect-[3/4] bg-muted rounded-2xl shadow-2xl flex items-center justify-center">
        <span class="text-muted-foreground">Miejsce na plakat</span>
      </div>
    </div>
  </div>
</Layout>
```

- [ ] **Step 2: Commit**

```bash
git add src/pages/index.astro
git commit -m "feat: implement hero section"
```

## Chunk 2: Verification

### Task 2: Verify Standards

- [ ] **Step 1: Run build, lint, and typecheck**

Run: `npm run lint && npm run typecheck && npm run build`
Expected: PASS

- [ ] **Step 2: Final commit**

```bash
git commit -am "chore: verify hero section implementation"
```
