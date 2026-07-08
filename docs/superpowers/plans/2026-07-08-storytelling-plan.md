# Storytelling Section Implementation Plan

> **For agentic workers:** REQUIRED: Use superpowers:executing-plans to implement this plan. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Implement the Storytelling section in `src/pages/index.astro`.

**Architecture:** Use a focused, centered content container with narrative-focused typography.

**Tech Stack:** Astro, Tailwind CSS (v4).

---

## Chunk 1: Implementation

### Task 1: Update `src/pages/index.astro`

**Files:**
- Modify: `src/pages/index.astro`
- Create: `src/lib/story-content.ts`

- [ ] **Step 1: Create `src/lib/story-content.ts`**

```typescript
export const storyContent = {
  heading: "Nie znajdziesz tych kadrów w banku stockowym.",
  body: "Większość sklepów oferuje tysiące wzorów, które wiszą w każdym biurze. Ja robię inaczej. Każdy plakat, który tutaj znajdziesz, to kadr, który sam uchwyciłem podczas moich europejskich wypraw. To nie są \"obrazki do wnętrz\" – to wspomnienia, światło i emocje, które zamknąłem w cyfrowym formacie dla Ciebie. Oferuję tylko limitowane nakłady plików cyfrowych, abyś mógł stworzyć przestrzeń, która jest tak unikalna, jak Twoje wspomnienia."
}
```

- [ ] **Step 2: Update `src/pages/index.astro` to include Storytelling section**

```astro
---
import Layout from "@/layouts/main.astro"
import { Button } from "@/components/ui/button"
import { heroContent } from "@/lib/hero-content"
import { storyContent } from "@/lib/story-content"
---

<Layout>
  <!-- Hero Section -->
  <!-- ... existing hero ... -->
  
  <!-- Storytelling Section -->
  <section class="py-24 px-6 bg-background">
    <div class="max-w-2xl mx-auto">
      <h2 class="text-3xl md:text-4xl font-bold tracking-tight text-foreground">
        {storyContent.heading}
      </h2>
      <p class="text-lg text-muted-foreground mt-8 leading-relaxed border-l-4 border-primary pl-6">
        {storyContent.body}
      </p>
    </div>
  </section>
</Layout>
```

- [ ] **Step 3: Commit**

```bash
git add src/pages/index.astro src/lib/story-content.ts
git commit -m "feat: implement storytelling section"
```

## Chunk 2: Verification

### Task 2: Verify Standards

- [ ] **Step 1: Run build and lint**

Run: `npm run lint && npm run typecheck && npm run build`
Expected: PASS

- [ ] **Step 2: Final commit**

```bash
git commit -am "chore: verify storytelling implementation"
```
