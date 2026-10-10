# REKA Landing Page — Brand & Design Brief
> Attach this file to any Claude chat building, refining, or reviewing the REKA marketing website.
> It includes every colour value, typography spec, layout pattern, and copy rule needed.
> Combine with REKA_UNIVERSAL_BRIEF.md for company/positioning facts.
> Last updated: June 2026

---

## 1. The landing page's job

The site positions REKA as the applied-AI and automation R&D company that works at the physical edge — roads, factories, crowds, machines — not just screens. Every section should feel precise and technically credible, not startup-generic. The tone is confident without being loud.

---

## 2. Complete colour system

### 2.1 CSS custom properties (copy this block into every project)

```css
:root {
  /* ── Brand orange ───────────────────────────────── */
  --c-brand:       #FB9800;   /* the one official orange */
  --c-brand-hi:    #FFB23E;   /* hover / glow on dark */
  --c-brand-dk:    #E65D01;   /* pressed / dark gradient end */

  /* ── Dark surfaces (hero, dark sections) ────────── */
  --c-dark-0:      #0B0B0C;   /* primary dark bg */
  --c-dark-1:      #161618;   /* cards / panels on dark */
  --c-dark-2:      #1D1D20;   /* raised elements on dark */
  --c-dark-3:      #26262C;   /* borders on dark */

  /* ── Light surfaces (public sections) ──────────── */
  --c-light-bg:    #F7F6F3;   /* primary light surface (barely warm) */
  --c-light-panel: #FFFFFF;   /* cards / panels on light */
  --c-light-border:#E5E4E1;   /* borders on light */

  /* ── Text ───────────────────────────────────────── */
  --c-ink:         #1D1D1D;   /* body text on light */
  --c-ink-2:       #565656;   /* secondary text on light */
  --c-ink-3:       #9A9A9A;   /* captions / meta on light */
  --c-ink-dark:    #F1F1F0;   /* body text on dark */
  --c-ink-dark-2:  #B9B9BD;   /* secondary text on dark */
  --c-ink-dark-3:  #76767C;   /* captions / meta on dark */

  /* ── Product families ───────────────────────────── */
  --c-harmonik:    #6040CC;   /* PLExyz purple   (Harmonik) */
  --c-kinetik:     #1AB89C;   /* OVERride teal   (Kinetik)  */
  --c-heuristik:   #1268F7;   /* AntaraX blue    (Heuristik)*/
  --c-esoterik:    #501643;   /* Tinara maroon   (Esoterik) */

  /* ── Typography ─────────────────────────────────── */
  --font-ui:       'Poppins', system-ui, sans-serif;
  --font-mono:     'JetBrains Mono', ui-monospace, monospace;
}
```

---

### 2.2 Colour reference — all values

#### Brand orange family
| Role | Hex | RGB | CMYK | Usage |
|---|---|---|---|---|
| Brand orange | `#FB9800` | 251, 152, 0 | C0 M39 Y100 K2 | Marks, CTAs, primary accents. The one official orange. |
| Highlight | `#FFB23E` | 255, 178, 62 | C0 M30 Y76 K0 | Hover glow on dark bg; icon fills on dark |
| Secondary | `#E65D01` | 230, 93, 1 | C0 M60 Y100 K10 | Pressed/hover on light; dark gradient end |

**Rule:** `#FB9800` is the only orange used in brand materials. `#f7941d`, `#E8742A`, `#FFA910` are retired.

---

#### Dark surface palette
| Token | Hex | RGB | Use |
|---|---|---|---|
| `--c-dark-0` | `#0B0B0C` | 11, 11, 12 | Hero bg, full-bleed dark sections |
| `--c-dark-1` | `#161618` | 22, 22, 24 | Cards, panels on dark bg |
| `--c-dark-2` | `#1D1D20` | 29, 29, 32 | Raised elements, nav on dark |
| `--c-dark-3` | `#26262C` | 38, 38, 44 | Borders, dividers on dark |

---

#### Light surface palette
| Token | Hex | RGB | Use |
|---|---|---|---|
| `--c-light-bg` | `#F7F6F3` | 247, 246, 243 | Primary page surface — warm off-white, not clinical |
| `--c-light-panel` | `#FFFFFF` | 255, 255, 255 | Cards, panels on light bg |
| `--c-light-border` | `#E5E4E1` | 229, 228, 225 | Borders, dividers on light |

---

#### Text
| Token | Hex | Use |
|---|---|---|
| `--c-ink` | `#1D1D1D` | Primary text on light surfaces |
| `--c-ink-2` | `#565656` | Secondary text, descriptions |
| `--c-ink-3` | `#9A9A9A` | Meta, captions, placeholders |
| `--c-ink-dark` | `#F1F1F0` | Primary text on dark surfaces |
| `--c-ink-dark-2` | `#B9B9BD` | Secondary text on dark |
| `--c-ink-dark-3` | `#76767C` | Meta, captions on dark |

---

#### Product family colours — full ramps
| Family | Light tint | Mid | Primary | Dark / nav | Product |
|---|---|---|---|---|---|
| Harmonik | `#C8BDE8` | `#865ACE` | `#6040CC` | `#241E58` | PLExyz |
| Kinetik | `#BAE4E1` | `#6AD1BF` | `#1AB89C` | `#063028` | OVERride |
| Heuristik | `#6AAEFF` | `#0496FF` | `#1268F7` | `#0D2850` | AntaraX |
| Esoterik | `#CAB9C7` | `#8D6885` | `#501643` | `#2D0A22` | Tinara |

**Usage on landing page:**
- Product section backgrounds: family dark bg shade
- Product cards: family primary as accent / border
- Product icons / marks: family primary
- Product section text: `#F1F1F0` (light ink on dark bg)

---

#### Secondary / document colours
| Name | Hex | Use |
|---|---|---|
| Products navy | `#274677` | Internal document tagging — not for web UI |
| Services maroon | `#501643` | Internal document tagging — not for web UI |

---

#### Accent libraries (illustration & graphics only — never UI)
| Library | Colours |
|---|---|
| Bold neon | `#00B3FF` `#00F0FF` `#3B72FF` `#FF5689` `#FF5757` `#FF7A00` |
| Soft pastel | `#ABC1F9` `#CBE2F7` `#ABE1F8` `#A6F3F8` `#F8CEDA` `#F9B6B6` `#F7DCC4` |

---

### 2.3 Tested colour combinations (use these, not raw swatches)

#### Core pairings
| Foreground | Background | Contrast | Use case |
|---|---|---|---|
| `#FB9800` | `#0B0B0C` | 8.4:1 AAA | Orange on dark — hero accents, marks |
| `#F1F1F0` | `#0B0B0C` | 18.7:1 AAA | Body text on dark |
| `#F1F1F0` | `#161618` | 16.2:1 AAA | Card text on dark |
| `#1D1D1D` | `#F7F6F3` | 16.8:1 AAA | Body text on light |
| `#E65D01` | `#F7F6F3` | 4.7:1 AA | Amber link text on light |
| `#FFB23E` | `#0B0B0C` | 6.1:1 AA | Hover / highlight on dark |
| `#FB9800` | `#F7F6F3` | 2.2:1 — | Orange fill only on light — NOT for body text |

**Note:** `#FB9800` on white/light fails text contrast. Use it as a fill, icon colour, or border — never as inline text on light backgrounds. Use `#E65D01` for orange text on light.

#### Product section pairings
| Family | Accent on dark nav | Text on dark |
|---|---|---|
| Harmonik / PLExyz | `#6040CC` nav + `#A784F1` active text | `#F1F1F0` |
| Kinetik / OVERride | `#1AB89C` nav + `#7DE8D5` active text | `#F1F1F0` |
| Heuristik / AntaraX | `#1268F7` nav + `#6AAEFF` active text | `#F1F1F0` |
| Esoterik / Tinara | `#501643` nav + `#B87AA0` active text | `#F1F1F0` |

---

## 3. Typography

### Font import
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500;600&display=swap" rel="stylesheet">
```

### Type scale for landing page

```css
/* Hero / cover headlines */
.t-hero  { font-family: var(--font-ui); font-size: clamp(2.6rem, 1.4rem + 5vw, 5rem);   font-weight: 800; letter-spacing: -0.04em; line-height: 1.0; }

/* Section headings */
.t-h1    { font-family: var(--font-ui); font-size: clamp(2rem,   1.2rem + 3.5vw, 3.4rem); font-weight: 800; letter-spacing: -0.03em; line-height: 1.05; }
.t-h2    { font-family: var(--font-ui); font-size: clamp(1.5rem, 1rem + 2vw, 2.4rem);    font-weight: 700; letter-spacing: -0.02em; line-height: 1.1; }
.t-h3    { font-family: var(--font-ui); font-size: 1.2rem;  font-weight: 700; letter-spacing: -0.01em; }

/* Body */
.t-body  { font-family: var(--font-ui); font-size: 1rem;    font-weight: 400; line-height: 1.65; }
.t-lead  { font-family: var(--font-ui); font-size: 1.1rem;  font-weight: 400; line-height: 1.6; }
.t-small { font-family: var(--font-ui); font-size: 0.875rem;font-weight: 400; line-height: 1.5; }

/* Mono / labels */
.t-label { font-family: var(--font-mono); font-size: 0.7rem; font-weight: 500; letter-spacing: 0.14em; text-transform: uppercase; }
.t-data  { font-family: var(--font-mono); font-size: 2rem;   font-weight: 600; letter-spacing: -0.04em; }
.t-code  { font-family: var(--font-mono); font-size: 0.875rem; font-weight: 400; }
```

---

## 4. Visual language — web application

### 4.1 Chamfer cuts (not border-radius)
REKA UI uses polygon clip-paths, not rounded corners. Use these in CSS:

```css
/* Small chip / tag */
.chamfer-xs  { clip-path: polygon(5px 0, 100% 0, 100% calc(100% - 5px), calc(100% - 5px) 100%, 0 100%, 0 5px); }

/* Button / badge */
.chamfer-sm  { clip-path: polygon(7px 0, 100% 0, 100% calc(100% - 7px), calc(100% - 7px) 100%, 0 100%, 0 7px); }

/* Card */
.chamfer-md  { clip-path: polygon(12px 0, calc(100% - 12px) 0, 100% 12px, 100% calc(100% - 12px), calc(100% - 12px) 100%, 12px 100%, 0 calc(100% - 12px), 0 12px); }

/* Hero / large panel */
.chamfer-lg  { clip-path: polygon(20px 0, calc(100% - 20px) 0, 100% 20px, 100% calc(100% - 20px), calc(100% - 20px) 100%, 20px 100%, 0 calc(100% - 20px), 0 20px); }

/* Single-corner (top-right only) — outer frames, hero images */
.chamfer-tr  { clip-path: polygon(0 0, calc(100% - 28px) 0, 100% 28px, 100% 100%, 0 100%); }
```

**Never use `border-radius` for brand UI elements.** Exception: small avatars/circles use `border-radius: 50%`.

### 4.2 Dot grid texture
Signature REKA background texture — applied on content area backgrounds:

```css
/* On dark sections */
.dot-dark {
  background-image: radial-gradient(circle, rgba(255,255,255,0.05) 1px, transparent 1px);
  background-size: 20px 20px;
}

/* On light sections */
.dot-light {
  background-image: radial-gradient(circle, rgba(0,0,0,0.055) 1px, transparent 1px);
  background-size: 20px 20px;
}
```

### 4.3 Orange usage rules for the landing page
- Orange on dark is always safe — use freely for icons, borders, labels, accent text
- Orange on light fails text contrast — use as fill, border, or icon fill only
- For orange-coloured inline text on light, use `#E65D01` (passes AA)
- Orange should occupy ~10% of any given section's surface area maximum
- The CTA button is the primary orange expression — one per viewport

### 4.4 Section rhythm
Alternate between dark and light sections. Typical pattern:

```
Hero          → dark (#0B0B0C)
Feature intro → dark or light
Features      → light (#F7F6F3), white panels
Products      → dark, each sub-section uses its family dark bg
Proof         → dark
CTA           → dark with strong orange
Footer        → near-black (#0B0B0C)
```

---

## 5. Landing page components

### 5.1 Navigation bar

```css
.navbar {
  position: sticky; top: 0; z-index: 50;
  background: rgba(11, 11, 12, 0.95);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid rgba(255,255,255,0.06);
  padding: 0 clamp(1.5rem, 5vw, 3rem);
  height: 60px;
  display: flex; align-items: center; gap: 2rem;
}
.navbar-logo { color: #F1F1F0; font-weight: 700; }
.navbar-link { color: #B9B9BD; font-size: 0.875rem; text-decoration: none; transition: color .15s; }
.navbar-link:hover { color: #F1F1F0; }
.navbar-cta {
  margin-left: auto;
  background: #FB9800; color: #0B0B0C; font-weight: 600; font-size: 0.875rem;
  padding: 8px 20px; text-decoration: none;
  clip-path: polygon(7px 0, 100% 0, 100% calc(100% - 7px), calc(100% - 7px) 100%, 0 100%, 0 7px);
}
.navbar-cta:hover { background: #FFB23E; }
```

### 5.2 Hero section

```css
.hero {
  min-height: 100svh;
  background: #0B0B0C;
  background-image: radial-gradient(circle, rgba(255,255,255,0.05) 1px, transparent 1px);
  background-size: 20px 20px;
  display: flex; flex-direction: column; justify-content: center;
  padding: clamp(4rem, 10vw, 8rem) clamp(1.5rem, 5vw, 4rem);
}
.hero-kicker {
  font-family: var(--font-mono); font-size: 0.72rem; letter-spacing: 0.2em;
  text-transform: uppercase; color: #E65D01;
  display: flex; align-items: center; gap: 0.6em; margin-bottom: 1.2rem;
}
.hero-kicker::before {
  content: ""; width: 9px; height: 9px; background: #FB9800;
  clip-path: polygon(50% 0,60% 40%,100% 50%,60% 60%,50% 100%,40% 60%,0 50%,40% 40%);
}
.hero-headline { color: #F1F1F0; margin-bottom: 1.4rem; }
.hero-headline em { font-style: normal; color: #FB9800; }
.hero-lead { color: #B9B9BD; max-width: 36rem; margin-bottom: 2.4rem; }
.hero-actions { display: flex; gap: 1rem; flex-wrap: wrap; }

/* Primary CTA */
.btn-primary {
  background: #FB9800; color: #0B0B0C; font-weight: 700; font-size: 0.95rem;
  padding: 14px 28px; text-decoration: none; display: inline-block;
  clip-path: polygon(9px 0, 100% 0, 100% calc(100% - 9px), calc(100% - 9px) 100%, 0 100%, 0 9px);
  transition: background .15s;
}
.btn-primary:hover { background: #FFB23E; }

/* Secondary CTA */
.btn-secondary {
  border: 1px solid rgba(255,255,255,0.2); color: #F1F1F0; font-weight: 500; font-size: 0.95rem;
  padding: 14px 28px; text-decoration: none; display: inline-block;
  clip-path: polygon(9px 0, 100% 0, 100% calc(100% - 9px), calc(100% - 9px) 100%, 0 100%, 0 9px);
  background: transparent; transition: border-color .15s, color .15s;
}
.btn-secondary:hover { border-color: #FB9800; color: #FB9800; }
```

**Hero copy pattern:**
```
KICKER:    "AI for the physical world"  ← mono, orange, uppercase
H1:        "Built on [em]Southeast Asian[/em] roads."
LEAD:      "REKA is one of the very few independent commercial R&D companies
            in Southeast Asia building AI for the physical world."
CTA:       "See what we build"  →  "Talk to us"
```

### 5.3 Feature / capability cards

```css
.feature-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 16px;
}
.feature-card {
  background: #161618; border: 1px solid rgba(255,255,255,0.07);
  padding: 24px;
  clip-path: polygon(0 0, calc(100% - 14px) 0, 100% 14px, 100% 100%, 0 100%);
}
.feature-card-icon {
  width: 36px; height: 36px; margin-bottom: 16px;
  color: #FB9800;
}
.feature-card-title { color: #F1F1F0; font-weight: 600; margin-bottom: 8px; }
.feature-card-body  { color: #B9B9BD; font-size: 0.875rem; line-height: 1.6; }
```

### 5.4 Product family section
Each product gets a section with its family dark background:

```css
.product-section-harmonik  { background: #241E58; } /* PLExyz */
.product-section-kinetik   { background: #063028; } /* OVERride */
.product-section-heuristik { background: #0D2850; } /* AntaraX */
.product-section-esoterik  { background: #2D0A22; } /* Tinara */

/* Product accent dot / tag */
.product-tag {
  font-family: var(--font-mono); font-size: 0.62rem; letter-spacing: 0.12em;
  text-transform: uppercase; padding: 4px 10px;
  border: 1px solid currentColor; display: inline-block; margin-bottom: 1rem;
}
```

### 5.5 Proof / credential bar (the milestone strip)

```
2016 — Malaysia's first self-driving car on open roads
Ongoing — Autoware Foundation member
2019 — Murata smart-city sensing partnership
2022 — Frost & Sullivan Best Crowd Analytics award
```

Layout: horizontal scrollable strip with mono font, orange year, muted description. Dark background. Use `font-family: var(--font-mono)`.

### 5.6 Footer

```css
.footer {
  background: #0B0B0C;
  border-top: 1px solid rgba(255,255,255,0.06);
  padding: clamp(3rem, 6vw, 5rem) clamp(1.5rem, 5vw, 4rem);
}
.footer-logo  { margin-bottom: 2rem; }
.footer-links { display: flex; gap: 2rem; flex-wrap: wrap; }
.footer-link  { color: #76767C; font-size: 0.875rem; text-decoration: none; }
.footer-link:hover { color: #F1F1F0; }
.footer-legal {
  margin-top: 2.4rem; padding-top: 1.6rem;
  border-top: 1px solid rgba(255,255,255,0.06);
  font-family: var(--font-mono); font-size: 0.62rem;
  letter-spacing: 0.08em; color: #76767C;
}
```

---

## 6. Copy rules for landing page

1. **No em dashes** — use commas, parentheses, or a new sentence.
2. **No currency** — all ROI claims as multiples (2×) or percentages, flagged `(illustrative)`.
3. **"Malaysia's first"** self-driving car on open roads (2016). Never "Southeast Asia's first".
4. **"Founder"** not CEO.
5. **No fabricated metrics** — flag all illustrative data explicitly.
6. **Keep superlatives honest** — REKA does not appear in commercial rankings; do not claim "top" or "leading" without an external citation.
7. **Positioning line** — "One of the very few independent commercial R&D companies in Southeast Asia building AI for the physical world." Use this verbatim in the about/positioning section.

---

## 7. Accessibility quick-checks

- All body text on dark: min 4.5:1 (currently 18.7:1 with `#F1F1F0` on `#0B0B0C`)
- Orange on dark backgrounds: ✓ (8.4:1 AAA)
- Orange as inline text on light: ✗ — use `#E65D01` instead
- Always provide `alt` text for logo and product marks
- Interactive elements min 44×44px touch target
- Focus rings visible — do not suppress `:focus-visible`

---

## 8. What not to do on the landing page

- Do not use `border-radius` for feature cards, buttons, or content panels
- Do not make orange the dominant surface colour — it is an accent
- Do not use `#f7941d`, `#E8742A`, `#0062FB` — retired colours
- Do not claim "Southeast Asia's first" for any product
- Do not use drop shadows or blurs on UI elements (decorative textures only)
- Do not use Poppins below weight 400 or above weight 800

---

## 9. Google Fonts import (production-ready)

```html
<!-- In <head> -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500;600&display=swap" rel="stylesheet">
```
