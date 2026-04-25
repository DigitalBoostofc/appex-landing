# Theme — AppexCRM Landing Page

## Stack
- Plain HTML/CSS/JS (no framework, no build step)
- Fonts: `Inter` (body), `JetBrains Mono` (numbers/code)
- Dark mode: toggled via `html.dark` class, CSS variables swap automatically

## CSS Variables (`:root` / `html.dark`)

```css
:root {
  --brand:   #635BFF;
  --brand2:  #8B5CF6;
  --pink:    #EC4899;
  --green:   #10B981;
  --amber:   #F59E0B;

  /* Page bg */
  --bg:      linear-gradient(180deg,#FDFBFF 0%,#F8F5FF 50%,#FFF5FA 100%);
  --surface: #ffffff;
  --ink1:    #0A0E1A;   /* headings */
  --ink2:    #425466;   /* body text */
  --ink3:    #8898AA;   /* captions / placeholders */
  --edge:    rgba(0,0,0,0.06);
  --edge2:   rgba(0,0,0,0.08);

  /* Mock UI (inside showcase cards) */
  --mock-bg:      #F6F9FC;
  --mock-surface: #FFFFFF;
  --mock-ink1:    #0F172A;
  --mock-ink2:    #425466;
  --mock-ink3:    #8898AA;
  --mock-edge:    rgba(0,0,0,0.06);
  --mock-edge2:   rgba(0,0,0,0.08);
  --mock-sidebar: #FFFFFF;
}

html.dark {
  --bg:      linear-gradient(180deg,#0A0A14 0%,#0F0A1F 50%,#1A0A1F 100%);
  --surface: #14141F;
  --ink1:    #F4F4F8;
  --ink2:    #A8A8BE;
  --ink3:    #7A7A95;
  --edge:    rgba(255,255,255,0.06);
  --edge2:   rgba(255,255,255,0.10);

  --mock-bg:      #0F0F12;
  --mock-surface: #17171A;
  --mock-ink1:    #F5F5F7;
  --mock-ink2:    #A1A1AA;
  --mock-ink3:    #6B6B73;
  --mock-edge:    rgba(255,255,255,0.06);
  --mock-edge2:   rgba(255,255,255,0.10);
  --mock-sidebar: #17171A;
}
```

## Gradients (used repeatedly)
- Primary brand: `linear-gradient(135deg,#635BFF,#8B5CF6)`
- Brand-to-pink: `linear-gradient(135deg,#635BFF,#8B5CF6 50%,#EC4899)`
- Pink-to-amber: `linear-gradient(135deg,#EC4899,#F59E0B)`
- Text grad: `background: linear-gradient(135deg,#635BFF 0%,#8B5CF6 45%,#EC4899 100%)` + `-webkit-background-clip:text`

## Typography Scale
| Use | Size | Weight | Font |
|-----|------|--------|------|
| Hero H1 | clamp(52px,8vw,86px) | 700 | Inter |
| Section title | clamp(36px,5vw,52px) | 700 | Inter |
| Section desc | 18px | 400 | Inter |
| Feature name | 19px | 700 | Inter |
| Body / feature desc | 14px | 400 | Inter |
| Nav links | 14px | 500 | Inter |
| Badge / caption | 12-13px | 600 | Inter |
| Mono numbers | varies | 600-700 | JetBrains Mono |

## Spacing & Radius
- Section padding: `120px 48px` (desktop), `64px 16px` (mobile ≤768px)
- Card border-radius: 20px (feature), 24-28px (showcase/pricing), 36px (CTA box)
- Button border-radius: 999px (pills), 12-14px (rectangular)
- Nav height: 68px

## Shadows
- Primary button: `0 12px 28px rgba(99,91,255,.4)`
- Card: `0 4px 20px rgba(99,91,255,.06)`
- Featured plan: `0 20px 48px rgba(99,91,255,.3)`

## Responsive Breakpoints
- `≤900px`: showcase-grid stacks, pricing cards stack
- `≤768px`: nav collapses to hamburger, section padding reduces, chip-wa/chip-rev hidden
- `≤480px`: hero kanban height 200px, im-sidebar narrows to 160px
