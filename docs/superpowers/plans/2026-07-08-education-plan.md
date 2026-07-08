# Education Section Implementation Plan

> **For agentic workers:** REQUIRED: Use superpowers:executing-plans to implement this plan. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Implement the "Education/Guide" section in `src/pages/index.astro`.

**Architecture:** Use a card-based grid layout for the guide's key points.

**Tech Stack:** Astro, Tailwind CSS (v4), shadcn/ui.

---

## Chunk 1: Implementation

### Task 1: Update `src/pages/index.astro`

**Files:**
- Create: `src/lib/education-content.ts`
- Modify: `src/pages/index.astro`

- [ ] **Step 1: Create `src/lib/education-content.ts`**

```typescript
export const educationContent = {
  heading: "Jak uzyskać efekt galerii sztuki we własnym domu?",
  body: "Boisz się, że wydruk wyjdzie blady lub niewyraźny? Przygotowałem dla Ciebie krótki poradnik (do pobrania za darmo), w którym tłumaczę:",
  points: [
    {
      title: "Głębia kolorów",
      description: "Na jakim papierze najlepiej drukować, aby uzyskać głębię kolorów."
    },
    {
      title: "Proporcje",
      description: "Jakie proporcje dobrać do wybranego rozmiaru ramy."
    },
    {
      title: "Drukarnie",
      description: "Gdzie szukać profesjonalnej drukarni, by jakość była identyczna z oryginałem."
    }
  ],
  cta: "Pobierz darmowy poradnik druku"
}
```

- [ ] **Step 2: Add Education section to `src/pages/index.astro`**

```astro
---
import { educationContent } from "@/lib/education-content"
// ... existing imports
---

<!-- ... Scarcity Section ... -->

<!-- Education Section -->
<section class="max-w-4xl mx-auto px-6 py-24">
  <div class="text-center">
    <h2 class="text-3xl md:text-4xl font-bold tracking-tight text-foreground">
      {educationContent.heading}
    </h2>
    <p class="text-lg text-muted-foreground mt-6 leading-relaxed">
      {educationContent.body}
    </p>
  </div>
  
  <div class="grid sm:grid-cols-3 gap-6 mt-12">
    {educationContent.points.map((point) => (
      <div class="bg-card p-6 rounded-xl border border-border text-center">
        <h3 class="font-semibold text-foreground">{point.title}</h3>
        <p class="text-sm text-muted-foreground mt-3">{point.description}</p>
      </div>
    ))}
  </div>

  <div class="text-center mt-12">
    <Button size="lg">{educationContent.cta}</Button>
  </div>
</section>
```

- [ ] **Step 3: Commit**

```bash
git add src/pages/index.astro src/lib/education-content.ts
git commit -m "feat: implement education section"
```

## Chunk 2: Verification

### Task 2: Verify Standards

- [ ] **Step 1: Run build and lint**

Run: `npm run lint && npm run typecheck && npm run build`
Expected: PASS

- [ ] **Step 2: Final commit**

```bash
git commit -am "chore: verify education implementation"
```
