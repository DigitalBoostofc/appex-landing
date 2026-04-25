# Routes — AppexCRM Landing Page

> This is a single-page static site. There is only one HTML file and no router.

## File Structure
```
appex-landing/
├── index.html          ← entire app (CSS + HTML + JS)
├── appex-logo.png      ← logo (used in footer)
└── assets/
    ├── appex-logo.png  ← logo (used in nav)
    ├── appex-logo.svg
    ├── crm-kanban-light.png  ← hero screenshot (light mode)
    └── crm-kanban-dark.png   ← hero screenshot (dark mode)
```

## Page Sections (anchor nav)

| Anchor | Section | Class |
|--------|---------|-------|
| (top) | Hero | `.hero` |
| `#recursos` | Features grid | `.features` |
| `#pricing` | Pricing + billing toggle | `.pricing` |
| (no anchor) | Showcase (inbox + dashboard) | `.showcase` |
| (no anchor) | Feature Compare Table | `.feat-compare` |
| (no anchor) | FAQ | `.pricing-faq` |
| (no anchor) | CTA | `.cta` |

## Nav Links
```html
<a href="#">Produto</a>
<a href="#recursos">Recursos</a>
<a href="#pricing">Preços</a>
<a href="#">Contato</a>
```

## Section Order (top → bottom)
1. Nav (`<nav class="nav">`)
2. Mobile drawer (`<nav class="nav-drawer">`)
3. Hero (`<section class="hero">`)
4. Features (`<section id="recursos" class="features reveal">`)
5. Showcase (`<section class="showcase reveal">`)
6. Pricing (`<section id="pricing" class="pricing reveal">`)
7. Feature Compare (`<section class="feat-compare reveal">`)
8. FAQ (`<div class="pricing-faq reveal">`)
9. CTA (`<section class="cta reveal">`)
10. Footer (`<footer>`)
