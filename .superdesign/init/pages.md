# Pages — AppexCRM Landing Page

> Single page: `index.html`. All dependencies are self-contained inline.

## index.html

Complete dependency tree (everything inline, no imports):

```
index.html
├── <style> (inline CSS — all styles)
│   ├── Reset
│   ├── CSS Variables (:root / html.dark)
│   ├── .page shell
│   ├── .blob + #cursorGlow (background FX)
│   ├── .nav + .theme-toggle + .nav-hamburger
│   ├── .nav-drawer (mobile)
│   ├── .hero + .hero-screenshot + .chip-wrap
│   ├── .features + .feature-card
│   ├── .showcase + .showcase-card
│   │   ├── .im* (Inbox Mock components)
│   │   └── .dm* (Dashboard Mock components)
│   ├── .feat-compare + .feat-table (Feature Compare)
│   ├── .pricing + .billing-toggle + .plan / .plan-featured
│   ├── .compare (compare grid inside pricing)
│   ├── .pricing-faq + .faq-item
│   ├── .cta + .cta-box
│   ├── footer
│   ├── .reveal (scroll animation)
│   └── @media breakpoints (900px, 768px, 480px)
│
├── External fonts (Google Fonts CDN)
│   ├── Inter (400, 500, 600, 700)
│   └── JetBrains Mono (500, 700)
│
├── assets/appex-logo.png (nav logo)
├── assets/crm-kanban-light.png (hero screenshot)
├── assets/crm-kanban-dark.png (hero screenshot dark)
├── appex-logo.png (footer logo)
│
└── <script> (inline JS)
    ├── Mobile hamburger toggle
    ├── Theme toggle (html.dark class)
    ├── Parallax + cursor glow (rAF lerp loop)
    ├── Billing toggle (pill animation + plan card switch)
    └── Scroll reveal (IntersectionObserver)
```

## When designing for this page

Pass the entire `index.html` as context since all CSS + HTML + JS are in one file.
For section-specific work, note the line ranges:
- Styles: lines 11–636
- Nav HTML: lines 648–685
- Hero: lines 688–739
- Features: lines 742–757
- Showcase: lines 760–843
- Pricing: lines 846–894
- Feature Compare: lines 897–977
- FAQ: lines 980–1006
- CTA: lines 1009–1020
- Footer: lines 1023–1037
- JavaScript: lines 1042–1159
