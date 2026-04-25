# Components — AppexCRM Landing Page

> All components live inline in `index.html` (single file, no build). Code excerpts are CSS class definitions + representative HTML.

---

## Button: `.btn-primary`

```css
.btn-primary {
  height: 52px; padding: 0 26px; border-radius: 999px;
  background: linear-gradient(135deg,#635BFF,#8B5CF6);
  color: #fff; font-size: 15.5px; font-weight: 600;
  display: inline-flex; align-items: center; gap: 8px;
  box-shadow: 0 12px 28px rgba(99,91,255,.4);
  border: none; cursor: pointer; font-family: inherit;
}
```
```html
<a href="#" class="btn-primary">Testar 7 dias grátis
  <svg width="14" height="14" ...arrow icon...></svg>
</a>
```

---

## Button: `.btn-ghost`

```css
.btn-ghost {
  height: 52px; padding: 0 26px; border-radius: 999px;
  background: rgba(255,255,255,.8); backdrop-filter: blur(12px);
  border: 1px solid rgba(0,0,0,.08);
  color: var(--ink1); font-size: 15.5px; font-weight: 600;
  display: inline-flex; align-items: center; gap: 8px;
  cursor: pointer; font-family: inherit;
  transition: background .4s, border-color .4s, color .4s;
}
html.dark .btn-ghost { background: rgba(30,30,50,.6); border-color: rgba(255,255,255,.1); }
```

---

## Button: `.btn-cta` (CTA section)

```css
.btn-cta {
  height: 52px; padding: 0 28px; border-radius: 999px;
  background: linear-gradient(135deg,#fff,#f8f9fc);
  color: #635BFF; font-size: 16px; font-weight: 700;
  display: inline-flex; align-items: center; gap: 8px;
  box-shadow: 0 12px 28px rgba(0,0,0,.2);
  border: none; cursor: pointer; font-family: inherit;
}
```

---

## Section Badge

```css
.section-badge {
  display: inline-block; padding: 6px 14px; border-radius: 999px;
  background: linear-gradient(135deg,rgba(99,91,255,.12),rgba(236,72,153,.12));
  border: 1px solid rgba(99,91,255,.2);
  font-size: 12.5px; font-weight: 600; color: var(--brand);
  margin-bottom: 16px;
}
```
```html
<div class="section-badge">RECURSOS</div>
```

---

## Feature Card

```css
.feature-card {
  padding: 32px; border-radius: 20px;
  background: var(--surface); border: 1px solid var(--edge);
  box-shadow: 0 4px 20px rgba(99,91,255,.06);
  position: relative; overflow: hidden;
  transition: background .4s, border-color .4s, box-shadow .4s;
}
.feature-card-glow { position: absolute; top: -40px; right: -40px; width: 140px; height: 140px; border-radius: 50%; filter: blur(20px); pointer-events: none; }
.feature-icon { width: 56px; height: 56px; border-radius: 14px; font-size: 28px; display: flex; align-items: center; justify-content: center; margin-bottom: 18px; }
.feature-name { font-size: 19px; font-weight: 700; color: var(--ink1); margin-bottom: 8px; }
.feature-desc { font-size: 14px; color: var(--ink2); line-height: 1.55; }
```
```html
<div class="feature-card">
  <div class="feature-card-glow" style="background:rgba(99,91,255,.1)"></div>
  <div class="feature-icon" style="background:rgba(99,91,255,.1)">📊</div>
  <div class="feature-name">Funil Kanban completo</div>
  <div class="feature-desc">Múltiplos pipelines, etapas customizáveis...</div>
</div>
```

---

## FAQ Item

```css
.faq-item {
  padding: 24px 28px; border-radius: 18px;
  background: rgba(255,255,255,.6); border: 1px solid rgba(0,0,0,.05);
  backdrop-filter: blur(10px); margin-bottom: 12px;
  transition: background .4s, border-color .4s;
}
html.dark .faq-item { background: rgba(20,20,35,.6); border-color: rgba(255,255,255,.06); }
.faq-item summary { list-style: none; cursor: pointer; display: flex; justify-content: space-between; align-items: center; font-size: 16px; font-weight: 600; color: var(--ink1); }
.faq-item[open] summary .chev { transform: rotate(180deg); }
.faq-item .chev { transition: transform .3s; color: var(--brand); flex-shrink: 0; margin-left: 16px; }
.faq-item p { font-size: 14.5px; color: var(--ink2); line-height: 1.65; margin: 14px 0 0; }
```
```html
<details class="faq-item">
  <summary>Como funciona o teste? <span class="chev">▾</span></summary>
  <p>...</p>
</details>
```

---

## Check Item (plan feature)

```css
.check { width: 20px; height: 20px; border-radius: 10px; background: linear-gradient(135deg,#635BFF,#8B5CF6); display: inline-flex; align-items: center; justify-content: center; flex-shrink: 0; }
.plan-feat { display: flex; align-items: center; gap: 10px; font-size: 13.5px; color: var(--ink1); transition: color .4s; }
```
```html
<div class="plan-feat">
  <span class="check"><svg width="10" height="10" ...checkmark...></svg></span>
  Todos os recursos do AppexCRM
</div>
```

---

## Theme Toggle

```css
.theme-toggle {
  display: inline-flex; align-items: center; padding: 3px; border-radius: 999px;
  background: rgba(255,255,255,.7); border: 1px solid rgba(0,0,0,.08);
  backdrop-filter: blur(12px); cursor: pointer; position: relative; width: 142px;
  box-shadow: 0 4px 14px rgba(99,91,255,.1);
}
html.dark .theme-toggle { background: rgba(30,30,50,.7); border-color: rgba(255,255,255,.1); }
.theme-toggle-pill {
  position: absolute; top: 3px; left: 3px; width: 68px; height: 30px; border-radius: 999px;
  background: linear-gradient(135deg,#F59E0B,#EC4899);
  transition: left .35s cubic-bezier(.4,0,.2,1), background .4s;
}
html.dark .theme-toggle-pill { left: 71px; background: linear-gradient(135deg,#635BFF,#8B5CF6); }
.theme-opt { flex: 1; height: 30px; display: flex; align-items: center; justify-content: center; gap: 5px; font-size: 12px; font-weight: 600; position: relative; z-index: 1; color: #8898AA; }
.theme-opt.active { color: #fff; }
```

---

## Billing Toggle

```css
.billing-toggle {
  display: inline-flex; padding: 4px; border-radius: 999px;
  background: rgba(255,255,255,.7); backdrop-filter: blur(12px);
  border: 1px solid rgba(0,0,0,.08); position: relative;
  transition: background .4s, border-color .4s;
}
.billing-opt { padding: 10px 24px; border-radius: 999px; font-size: 14px; font-weight: 600; cursor: pointer; color: var(--ink3); position: relative; z-index: 1; display: inline-flex; align-items: center; gap: 8px; }
.billing-opt.active { color: #fff; }
.billing-pill {
  position: absolute; top: 4px; height: calc(100% - 8px);
  background: linear-gradient(135deg,#635BFF,#8B5CF6); border-radius: 999px;
  box-shadow: 0 6px 16px rgba(99,91,255,.35);
  transition: left .35s cubic-bezier(.4,0,.2,1), width .35s cubic-bezier(.4,0,.2,1);
}
.billing-badge { background: linear-gradient(135deg,#EC4899,#F59E0B); color: #fff; padding: 2px 8px; border-radius: 999px; font-size: 10.5px; font-weight: 700; }
```
```html
<div class="billing-toggle" id="billing-toggle">
  <div class="billing-pill" id="billing-pill"></div>
  <div class="billing-opt" data-b="monthly">Mensal</div>
  <div class="billing-opt active" data-b="annual">Anual <span class="billing-badge">-20%</span></div>
</div>
```

---

## Scroll Reveal

```css
.reveal { opacity: 0; }
.reveal.in { animation: revealIn 900ms cubic-bezier(.22,1,.36,1) forwards; }
@keyframes revealIn { from { opacity:0; transform:translateY(32px); } to { opacity:1; transform:translateY(0); } }
```
JS: `IntersectionObserver` with threshold 0.1 adds class `in` when element enters viewport.

---

## Animated Blob Background

```css
.blob { position: absolute; border-radius: 50%; filter: blur(40px); pointer-events: none; will-change: transform; }
.blob-1 { top: -120px; right: -120px; width: 480px; height: 480px; background: radial-gradient(circle,rgba(168,85,247,.28) 0%,transparent 70%); }
.blob-2 { top: 200px; left: -160px; width: 480px; height: 480px; background: radial-gradient(circle,rgba(99,91,255,.25) 0%,transparent 70%); }
.blob-3 { top: 1400px; right: 40px; width: 400px; height: 400px; background: radial-gradient(circle,rgba(236,72,153,.22) 0%,transparent 70%); }
```
JS: lerp-based parallax animates blobs on mouse move + scroll.
