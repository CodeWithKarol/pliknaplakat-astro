# Footer Implementation Plan

> **For agentic workers:** REQUIRED: Use superpowers:executing-plans to implement this plan. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Implement a trust-focused Footer for the landing page.

**Architecture:** Component-based footer structure with responsive 3-column layout.

**Tech Stack:** Astro, Tailwind CSS (v4).

---

## Chunk 1: Implementation

### Task 1: Create Footer Component

**Files:**
- Create: `src/components/Footer.astro`
- Modify: `src/layouts/main.astro`

- [ ] **Step 1: Create `src/components/Footer.astro`**

```astro
<footer class="bg-muted/30 py-16 px-6 mt-20">
  <div class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-12">
    <!-- Column 1: Identity -->
    <div>
      <h3 class="font-bold text-lg text-foreground">Plik na Plakat</h3>
      <p class="text-sm text-muted-foreground mt-4">
        Twoje zdjęcia. Twój klimat. Twój dom.
      </p>
    </div>
    
    <!-- Column 2: Offer -->
    <div>
      <h3 class="font-bold text-sm uppercase tracking-wider text-foreground">Oferta</h3>
      <ul class="space-y-3 mt-4 text-sm text-muted-foreground">
        <li><a href="#" class="hover:text-primary transition-colors">Kolekcja "Włoskie Lato"</a></li>
        <li><a href="#" class="hover:text-primary transition-colors">Kolekcja "Skandynawski Minimalizm"</a></li>
        <li><a href="#" class="hover:text-primary transition-colors">Kolekcja "Miejski Detal"</a></li>
        <li><a href="#" class="hover:text-primary transition-colors">Darmowy poradnik druku</a></li>
      </ul>
    </div>
    
    <!-- Column 3: Trust -->
    <div>
      <h3 class="font-bold text-sm uppercase tracking-wider text-foreground">Wsparcie</h3>
      <ul class="space-y-3 mt-4 text-sm text-muted-foreground">
        <li>Kontakt: <a href="mailto:pomoc@pliknaplakat.pl" class="hover:text-primary transition-colors">pomoc@pliknaplakat.pl</a></li>
        <li><a href="#" class="hover:text-primary transition-colors">Regulamin</a></li>
        <li><a href="#" class="hover:text-primary transition-colors">Polityka Prywatności</a></li>
      </ul>
    </div>
  </div>
  <div class="max-w-7xl mx-auto mt-16 pt-8 border-t border-border text-center text-xs text-muted-foreground">
    © 2026 Plik na Plakat
  </div>
</footer>
```

- [ ] **Step 2: Integrate into `src/layouts/main.astro`**

```astro
---
import "@/styles/global.css"
import Footer from "@/components/Footer.astro"
---

<html lang="pl">
  <head>
    <!-- ... -->
  </head>
  <body>
    <slot />
    <Footer />
  </body>
</html>
```

- [ ] **Step 3: Commit**

```bash
git add src/components/Footer.astro src/layouts/main.astro
git commit -m "feat: implement trust-focused footer"
```

## Chunk 2: Verification

### Task 2: Verify Standards

- [ ] **Step 1: Run build and lint**

Run: `npm run lint && npm run typecheck && npm run build`
Expected: PASS

- [ ] **Step 2: Final commit**

```bash
git commit -am "chore: verify footer implementation"
```
