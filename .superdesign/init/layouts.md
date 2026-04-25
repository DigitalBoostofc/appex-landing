# Layouts — AppexCRM Landing Page

> Single-page app. All layout lives in `index.html`. No shared layout files — everything is inline.

---

## Nav (`<nav class="nav">`)

```css
.nav {
  position: relative; z-index: 10;
  height: 68px; padding: 0 48px;
  display: flex; align-items: center; gap: 28px;
}
.nav-logo { display: flex; align-items: center; gap: 10px; }
.nav-logo-mark { width: 30px; height: 30px; border-radius: 7px; overflow: hidden; flex-shrink: 0; box-shadow: 0 4px 14px rgba(99,91,255,.4); }
.nav-logo-name { font-size: 16px; font-weight: 700; color: var(--ink1); letter-spacing: -.015em; }
.nav-links { display: flex; gap: 24px; font-size: 14px; font-weight: 500; color: var(--ink2); }
.nav-spacer { flex: 1; }
.nav-entry { font-size: 14px; font-weight: 500; color: var(--ink2); cursor: pointer; }
.nav-cta { height: 38px; padding: 0 18px; border-radius: 999px; background: linear-gradient(135deg,#635BFF,#8B5CF6); color: #fff; font-size: 13.5px; font-weight: 600; }

/* Mobile hamburger */
.nav-hamburger { display: none; flex-direction: column; justify-content: center; gap: 5px; width: 36px; height: 36px; border-radius: 8px; background: transparent; border: none; cursor: pointer; padding: 6px; }
.nav-hamburger span { display: block; height: 2px; border-radius: 2px; background: var(--ink2); transition: transform .3s, opacity .3s; }
.nav-hamburger.open span:nth-child(1) { transform: translateY(7px) rotate(45deg); }
.nav-hamburger.open span:nth-child(2) { opacity: 0; }
.nav-hamburger.open span:nth-child(3) { transform: translateY(-7px) rotate(-45deg); }

@media (max-width: 768px) {
  .nav { padding: 0 16px; gap: 8px; }
  .nav-links, .nav-entry, .nav-cta { display: none; }
  .nav-hamburger { display: flex; }
}
```

```html
<nav class="nav">
  <div class="nav-logo">
    <div class="nav-logo-mark"><img src="assets/appex-logo.png" alt="AppexCRM" /></div>
    <span class="nav-logo-name">AppexCRM</span>
  </div>
  <div class="nav-links">
    <a href="#">Produto</a>
    <a href="#recursos">Recursos</a>
    <a href="#pricing">Preços</a>
    <a href="#">Contato</a>
  </div>
  <div class="nav-spacer"></div>
  <button class="nav-hamburger" id="hamburger" aria-label="Menu" aria-expanded="false">
    <span></span><span></span><span></span>
  </button>
  <button class="theme-toggle" id="themeToggle">...</button>
  <span class="nav-entry">Entrar</span>
  <button class="nav-cta">Começar grátis ✨</button>
</nav>
```

---

## Mobile Nav Drawer (`<nav class="nav-drawer">`)

```css
.nav-drawer {
  display: none; position: absolute; top: 68px; left: 0; right: 0;
  background: var(--surface); border-bottom: 1px solid var(--edge);
  padding: 16px 20px 20px; flex-direction: column; gap: 4px; z-index: 99;
}
.nav-drawer.open { display: flex; }
.nav-drawer a { display: block; padding: 10px 12px; border-radius: 8px; font-size: 15px; font-weight: 500; color: var(--ink2); }
.nav-drawer-cta { margin-top: 8px; height: 46px; border-radius: 12px; background: linear-gradient(135deg,#635BFF,#8B5CF6); color: #fff; font-size: 15px; font-weight: 600; }
```

---

## Footer (`<footer>`)

```css
footer { padding: 48px 48px 32px; background: #0A0E1A; color: #fff; }
.footer-inner { max-width: 1280px; margin: 0 auto; display: flex; justify-content: space-between; gap: 40px; flex-wrap: wrap; }
.footer-logo { display: flex; align-items: center; gap: 10px; margin-bottom: 12px; }
.footer-logo-mark { width: 32px; height: 32px; border-radius: 8px; overflow: hidden; }
.footer-name { font-size: 15px; font-weight: 700; }
.footer-tagline { font-size: 13px; color: rgba(255,255,255,.5); max-width: 280px; line-height: 1.6; }
.footer-col-title { font-size: 12px; font-weight: 600; color: #fff; margin-bottom: 14px; text-transform: uppercase; letter-spacing: .06em; }
.footer-links { display: flex; flex-direction: column; gap: 10px; }
.footer-links a { font-size: 13px; color: rgba(255,255,255,.5); }
.footer-bottom { max-width: 1280px; margin: 40px auto 0; padding-top: 24px; border-top: 1px solid rgba(255,255,255,.08); display: flex; justify-content: space-between; flex-wrap: wrap; gap: 12px; font-size: 12px; color: rgba(255,255,255,.4); }

@media (max-width: 768px) {
  footer { padding: 40px 16px 24px; }
  .footer-inner { flex-direction: column; gap: 28px; }
}
```

```html
<footer>
  <div class="footer-inner">
    <div>
      <div class="footer-logo">
        <div class="footer-logo-mark"><img src="appex-logo.png" alt="AppexCRM" style="width:100%;height:100%;object-fit:cover;border-radius:8px;display:block;"></div>
        <span class="footer-name">AppexCRM</span>
      </div>
      <div class="footer-tagline">Feito no Brasil, para quem vende no Brasil. 🇧🇷</div>
    </div>
    <div><div class="footer-col-title">Produto</div><div class="footer-links"><a href="#">Funil</a><a href="#">Inbox</a><a href="#">Relatórios</a><a href="#">Automações</a></div></div>
    <div><div class="footer-col-title">Empresa</div><div class="footer-links"><a href="#">Clientes</a><a href="#">Contato</a><a href="#">Blog</a></div></div>
    <div><div class="footer-col-title">Recursos</div><div class="footer-links"><a href="#">Docs</a><a href="#">API</a><a href="#">Status</a></div></div>
  </div>
  <div class="footer-bottom">
    <div>© 2026 AppexCRM</div>
    <div class="footer-bottom-links"><a href="#">Termos</a><a href="#">Privacidade</a><a href="#">LGPD</a></div>
  </div>
</footer>
```

---

## Page Shell (`.page`)

```css
.page {
  background: var(--bg);
  color: var(--ink1);
  min-height: 100vh;
  overflow: hidden;
  position: relative;
  transition: background .5s ease, color .4s ease;
}
```
Contains: blobs, cursorGlow, nav, nav-drawer, all sections, footer.
