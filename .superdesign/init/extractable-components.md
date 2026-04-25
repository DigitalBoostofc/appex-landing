# Extractable Components — AppexCRM Landing Page

Components that appear across multiple contexts or are good candidates for reuse.

---

## 1. PillButton (`.btn-primary` / `.nav-cta` / `.btn-cta`)

Used in: hero CTAs, nav, CTA section, plan cards.

**Props:** `variant` (primary | ghost | cta | outline), `label`, `icon?`

Pattern: `border-radius: 999px`, gradient bg, flex + gap for icon.

---

## 2. SectionHeader (`.section-badge` + `.section-title` + `.section-desc`)

Used in: Features, Pricing, Feature Compare, Showcase.

**Props:** `badge`, `title` (supports `.grad` span), `desc?`

```html
<div class="section-badge">LABEL</div>
<h2 class="section-title">Main <span class="grad">Headline</span></h2>
<p class="section-desc">Supporting description text.</p>
```

---

## 3. FeatureCard (`.feature-card`)

Used in: Features section (8 cards in auto-fit grid).

**Props:** `icon` (emoji), `color` (rgba for glow + icon bg), `name`, `desc`

Grid: `repeat(auto-fit, minmax(300px, 1fr))`, gap 20px.

---

## 4. FaqItem (`<details class="faq-item">`)

Used in: FAQ section (6 items).

**Props:** `question`, `answer`

Native `<details>`/`<summary>` with CSS chevron rotation on `[open]`.

---

## 5. PlanCheckItem (`.plan-feat`)

Used in: Monthly plan (3 items), Annual plan (4 items).

**Props:** `label`

Pattern: gradient circle check icon + text, flex row, gap 10px.

---

## 6. AvatarStack (`.hero-avatars`)

Used in: Hero proof section.

**Props:** `initials[]`, `gradients[]`

Pattern: overlapping circles with `margin-left: -8px`, colored gradient bgs.

---

## 7. MockInbox (`.im` + all `.im-*` classes)

Used in: Showcase section (left card).

Full chat UI mock with sidebar, conversation list, message bubbles, typing indicator.

---

## 8. MockDashboard (`.dm` + all `.dm-*` classes)

Used in: Showcase section (right card).

KPI stats grid + bar chart + funnel visualization.

---

## 9. FloatingChip (`.chip-wrap` + `.chip`)

Used in: Hero section (WhatsApp notification chip + revenue chip).

**Props:** `rotation` (-3deg or 3deg), `animation-delay`, content slot.

Pattern: `animate: bob` (translateY oscillation), box-shadow tinted by brand.

---

## 10. HeroKanbanScreenshot (`.hero-kanban`)

Used in: Hero section.

Light/dark image swap via `opacity` transition on `html.dark`.

```html
<div class="hero-kanban">
  <img class="kanban-light" src="assets/crm-kanban-light.png" />
  <img class="kanban-dark"  src="assets/crm-kanban-dark.png" />
</div>
```

---

## 11. FeatureCompareTable (`.feat-table`)

Used in: Feature Compare section.

Categories as gradient header rows (`.feat-cat-row`), feature rows with ✓/— cells.
