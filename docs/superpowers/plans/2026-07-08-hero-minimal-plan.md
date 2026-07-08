# Minimalist Hero Section Implementation Plan

> **For agentic workers:** REQUIRED: Use superpowers:executing-plans to implement this plan. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Refactor the Hero section in `src/pages/index.astro` to a centered, minimalist design.

**Architecture:** Update existing Astro layout with focused Tailwind classes for centering and scale.

**Tech Stack:** Astro, Tailwind CSS (v4).

---

## Chunk 1: Implementation

### Task 1: Update `src/pages/index.astro`

**Files:**
- Modify: `src/pages/index.astro`

- [ ] **Step 1: Update markup to centered layout**

```astro
---
import Layout from "@/layouts/main.astro"
import { Button } from "@/components/ui/button"
import { heroContent } from "@/lib/hero-content"
---

<Layout>
  <div class="relative w-full overflow-hidden bg-white">
    <!-- Modern background gradient -->
    <div class="absolute inset-0 z-0 bg-gradient-to-br from-indigo-50 via-white to-white"></div>
    
    <!-- Centered content -->
    <div class="relative z-10 max-w-3xl mx-auto px-6 py-24 text-center">
      <h1 class="text-5xl md:text-6xl font-bold tracking-tight text-foreground leading-tight">
        {heroContent.heading}
      </h1>
      <p class="text-xl text-muted-foreground mt-6 leading-relaxed">
        {heroContent.subtitle}
      </p>
      <div class="flex flex-col sm:flex-row justify-center gap-4 mt-10">
        <Button size="lg">{heroContent.cta.primary}</Button>
        <a href="#" class="text-sm font-medium text-muted-foreground hover:text-foreground transition-colors py-3">
          {heroContent.cta.secondary}
        </a>
      </div>
    </div>
  </div>
</Layout>
```

- [ ] **Step 2: Commit**

```bash
git add src/pages/index.astro
git commit -m "refactor: implement minimalist centered hero"
```

## Chunk 2: Verification

### Task 2: Verify Standards

- [ ] **Step 1: Run build and lint**

Run: `npm run lint && npm run typecheck && npm run build`
Expected: PASS

- [ ] **Step 2: Final commit**

```bash
git commit -am "chore: verify minimalist hero implementation"
```
