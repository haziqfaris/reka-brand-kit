# REKA Public Stripe — Web Usage Guide
> How to use the REKA public/lanyard stripe on websites, in both horizontal and vertical orientations.
> Asset: `assets/reka-stripe-public.svg` · Native dimensions: 6143 × 119 px (52:1 ratio)
> Updated: June 2026

---

## What the public stripe is

The REKA public stripe is a wide decorative band of repeating instrument-panel motifs — tick marks, hatch runs, arrow panels, capsule tags, and a REKA lockup per repeat cycle. It is orange on transparent, so it reads over both dark and light backgrounds.

Use it as a visual system accent: header/footer dividers, hero overlays, section separators, sidebar accents, merchandise bands.

**Do not** distort, recolour, or crop mid-motif. Tile it; don't stretch it.

---

## 1. Setup — get the file

```
reka-brand-kit/
  assets/
    reka-stripe-public.svg    ← use this
    reka-stripe-official.svg  ← vertical letterhead stripe (different use)
```

The SVG is transparent-background, orange (#FB9800). It works over any surface.

---

## 2. Horizontal stripe (natural orientation)

### 2a. As a full-width band

```html
<div class="reka-stripe-h" aria-hidden="true"></div>
```

```css
.reka-stripe-h {
  width: 100%;
  height: 20px;           /* adjust 12px–40px to taste */
  background-image: url('assets/reka-stripe-public.svg');
  background-repeat: repeat-x;
  background-size: auto 100%;   /* height governs scale; width tiles */
  background-position: left center;
  flex-shrink: 0;
}
```

**Dark background variant** (orange reads clearly):
```css
.reka-stripe-h--dark {
  background-color: #0B0B0C;  /* add under the transparent stripe */
}
```

**Light background variant** (orange on warm light):
```css
.reka-stripe-h--light {
  background-color: #F7F6F3;
}
```

---

### 2b. As a section divider

```html
<!-- Between two sections -->
<section class="section-dark">...</section>
<div class="reka-stripe-h" aria-hidden="true"></div>
<section class="section-light">...</section>
```

```css
.reka-stripe-h {
  height: 16px;
  width: 100%;
  background: url('assets/reka-stripe-public.svg') repeat-x left center / auto 100%;
}
```

---

### 2c. As a sticky header accent (sits under the navbar)

```html
<nav class="navbar">...</nav>
<div class="reka-stripe-h" aria-hidden="true"></div>
```

```css
.navbar {
  position: sticky; top: 0; z-index: 50;
  background: rgba(11, 11, 12, 0.95);
  backdrop-filter: blur(12px);
}
/* Stripe sits beneath the navbar, scrolls with content */
.reka-stripe-h {
  position: sticky;
  top: 60px; /* match navbar height */
  z-index: 49;
  height: 14px;
  width: 100%;
  background: url('assets/reka-stripe-public.svg') repeat-x left center / auto 100%;
}
```

---

### 2d. As a footer top border

```html
<footer>
  <div class="reka-stripe-h" aria-hidden="true"></div>
  <div class="footer-content">...</div>
</footer>
```

```css
footer { background: #0B0B0C; }
footer .reka-stripe-h { height: 18px; }
```

---

### 2e. Using `<img>` instead of background (for simpler HTML)

```html
<img
  src="assets/reka-stripe-public.svg"
  class="reka-stripe-img"
  alt=""
  aria-hidden="true"
/>
```

```css
.reka-stripe-img {
  width: 100%;
  height: 20px;
  object-fit: cover;       /* tiles and fills */
  object-position: left;
  display: block;
}
```

---

## 3. Vertical stripe

The stripe is natively horizontal, so vertical deployment needs a CSS rotation approach. Two methods below — choose based on your layout context.

### 3a. Sidebar / left-edge accent (fixed width, flexible height)

Use a wrapper that is the final display size, with a rotated inner that carries the background.

```html
<aside class="sidebar">
  <div class="reka-stripe-v" aria-hidden="true"></div>
  <nav>...</nav>
</aside>
```

```css
/* The stripe column */
.reka-stripe-v {
  position: relative;
  width: 20px;        /* final display width of the stripe */
  height: 100%;       /* fill the sidebar height */
  overflow: hidden;
  flex-shrink: 0;
}

/* The inner element is the stripe, rotated into vertical */
.reka-stripe-v::before {
  content: '';
  position: absolute;
  /* Swap width and height — width = parent height, height = parent width */
  width: 100vh;       /* large enough to fill any height */
  height: 20px;       /* must match wrapper width */
  top: 0;
  left: 0;
  background: url('assets/reka-stripe-public.svg') repeat-x left center / auto 100%;
  transform-origin: 0 0;
  transform: rotate(90deg) translateY(-100%);
}
```

---

### 3b. Right-edge accent (flows down the right side of a section)

```html
<section class="feature-section">
  <div class="section-content">...</div>
  <div class="reka-stripe-v reka-stripe-v--right" aria-hidden="true"></div>
</section>
```

```css
.feature-section {
  display: flex;
  position: relative;
}
.section-content { flex: 1; }

.reka-stripe-v {
  position: relative;
  width: 18px;
  align-self: stretch;
  overflow: hidden;
  flex-shrink: 0;
}
.reka-stripe-v::before {
  content: '';
  position: absolute;
  width: 100vh;
  height: 18px;
  background: url('assets/reka-stripe-public.svg') repeat-x left center / auto 100%;
  transform-origin: 0 0;
  transform: rotate(90deg) translateY(-100%);
}
```

---

### 3c. Absolutely positioned vertical accent (hero overlays, cards)

Good for decorating the left or right edge of a card or hero panel without affecting layout.

```html
<div class="hero" style="position: relative; overflow: hidden;">
  <div class="reka-stripe-absolute-right" aria-hidden="true"></div>
  <!-- hero content -->
</div>
```

```css
.reka-stripe-absolute-right {
  position: absolute;
  right: 0; top: 0; bottom: 0;
  width: 16px;
  overflow: hidden;
}
.reka-stripe-absolute-right::before {
  content: '';
  position: absolute;
  height: 16px;
  width: 100%;
  min-width: 200px;
  background: url('assets/reka-stripe-public.svg') repeat-x left center / auto 100%;
  top: 0; left: 0;
  transform-origin: 0 0;
  transform: rotate(90deg) translateY(-100%);
  opacity: 0.6;  /* subtle on busy backgrounds */
}
```

---

## 4. Sizing reference

| Context | Height (horiz) / Width (vert) | Notes |
|---|---|---|
| Micro chip / tag | 8–10px | Almost invisible, purely textural |
| Compact header/footer | 12–16px | Good for most web headers |
| Standard band | 18–24px | Default — motifs read clearly |
| Prominent hero band | 28–40px | Full motif detail visible |
| Large-scale / hero | 48px+ | All detail crisp, use sparingly |

---

## 5. Opacity on different backgrounds

The stripe SVG is flat orange on transparent. Adjust opacity if needed:

```css
/* Full orange on dark — most legible */
.reka-stripe-h { opacity: 1; }

/* Softened on busy light backgrounds */
.reka-stripe-h--subtle { opacity: 0.55; }

/* Ghost / watermark on hero images */
.reka-stripe-h--ghost { opacity: 0.25; }
```

---

## 6. CSS custom property integration

```css
:root {
  --stripe-url: url('assets/reka-stripe-public.svg');
  --stripe-h: 20px;       /* default height */
  --stripe-h-lg: 32px;    /* large variant */
}

.reka-stripe-h {
  height: var(--stripe-h);
  background: var(--stripe-url) repeat-x left center / auto 100%;
}
```

---

## 7. Tailwind / utility class equivalent

If you use Tailwind, add this to your config:

```js
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      backgroundImage: {
        'reka-stripe': "url('/assets/reka-stripe-public.svg')",
      },
    },
  },
}
```

```html
<!-- Horizontal stripe -->
<div class="w-full h-5 bg-reka-stripe bg-repeat-x bg-left-center" aria-hidden="true"></div>
```

---

## 8. Common patterns — quick reference

```html
<!-- Under navbar -->
<div style="height:16px;width:100%;background:url('assets/reka-stripe-public.svg') repeat-x left/auto 100%"></div>

<!-- Top of footer -->
<div style="height:14px;width:100%;background:url('assets/reka-stripe-public.svg') repeat-x left/auto 100%"></div>

<!-- Left sidebar accent (20px wide, full height) -->
<div style="width:20px;height:100%;overflow:hidden;position:relative;flex-shrink:0">
  <div style="position:absolute;width:100vh;height:20px;background:url('assets/reka-stripe-public.svg') repeat-x left/auto 100%;transform-origin:0 0;transform:rotate(90deg) translateY(-100%)"></div>
</div>

<!-- Section separator -->
<hr style="border:0;height:18px;background:url('assets/reka-stripe-public.svg') repeat-x left/auto 100%;margin:0">
```

---

## 9. About the official document stripe

If you need a natively vertical stripe (for letterheads, right-margin accents, or print layouts), use `reka-stripe-official.svg` instead. It is 155 × 3508 px, portrait-native, and designed to sit along the edge of a document page.

```css
/* Official stripe as a left/right document margin accent */
.reka-stripe-official {
  width: 14px;
  height: 100%;
  background: url('assets/reka-stripe-official.svg') no-repeat top center / 100% auto;
}
```

Use the public stripe for web UI and repeating bands. Use the official stripe for print-style document layouts where a single tall instance runs full-height.

---

*Asset source: `reka-brand-kit/assets/reka-stripe-public.svg`*
*Brand colour: #FB9800 on transparent*
*Repeat period: ~3071 px (two motif cycles across 6143 px)*
