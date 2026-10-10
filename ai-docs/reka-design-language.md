# REKA Design Language
> Visual language rules for UI, illustrations, and brand materials.
> Updated: June 2026

## The mark — three forces
The REKA logomark decomposes into three symbolic parts:
- **Meniscus** — upper-left arc with ruled hatch lines = Order / Methodical / Structure
- **Scalpel** — diagonal blade through the disc = Discovery / Bold / Curiosity
- **Lightning** — lower-right arc with jagged bolt = Chaos / Abstract / Flashy

The wordmark uses a **lambda "A"** — the character that looks like Λ.

## Chamfer cuts (not border-radius)
REKA UI uses polygon clip-paths to create chamfered corners, not rounded corners.

```css
/* Micro — KPI cards, small chips */
clip-path: polygon(7px 0, calc(100% - 7px) 0, 100% 7px, 100% calc(100% - 7px),
                   calc(100% - 7px) 100%, 7px 100%, 0 calc(100% - 7px), 0 7px);

/* Medium — panels, side panels */
clip-path: polygon(9px 0, calc(100% - 9px) 0, 100% 9px, 100% calc(100% - 9px),
                   calc(100% - 9px) 100%, 9px 100%, 0 calc(100% - 9px), 0 9px);

/* Large — hero panels */
clip-path: polygon(12px 0, calc(100% - 12px) 0, 100% 12px, 100% calc(100% - 12px),
                   calc(100% - 12px) 100%, 12px 100%, 0 calc(100% - 12px), 0 12px);

/* Outer screen frame (one-corner only — top-right) */
clip-path: polygon(0 0, calc(100% - 24px) 0, 100% 24px, 100% 100%, 0 100%);
```

**Never use `border-radius` on brand UI elements.** Chamfer only.

## Dot grid texture
Subtle background texture used on all content areas:

```css
/* Light surfaces */
background-image: radial-gradient(circle, rgba(0,0,0,0.06) 1px, transparent 1px);
background-size: 20px 20px;

/* Dark surfaces */
background-image: radial-gradient(circle, rgba(255,255,255,0.042) 1px, transparent 1px);
background-size: 20px 20px;
```

## HUD corner brackets
Decorative bracket marks in the corners of hero panels. Use `#FB9800` or the family accent at 40% opacity.

```html
<svg viewBox="0 0 100 100" preserveAspectRatio="none" style="position:absolute;inset:0;width:100%;height:100%;pointer-events:none">
  <path d="M0 18 L0 0 L18 0"   fill="none" stroke="currentColor" stroke-width="1.8" opacity="0.4"/>
  <path d="M82 0 L100 0 L100 18"  fill="none" stroke="currentColor" stroke-width="1.8" opacity="0.4"/>
  <path d="M0 82 L0 100 L18 100"  fill="none" stroke="currentColor" stroke-width="1.8" opacity="0.4"/>
  <path d="M82 100 L100 100 L100 82" fill="none" stroke="currentColor" stroke-width="1.8" opacity="0.4"/>
</svg>
```

## Aesthetic principles
- **Instrument-panel / HUD:** Data readouts, mono labels, technical precision
- **Orange-on-dark:** The dominant expression. `#FB9800` on `#0B0B0C` or on family dark bg
- **Restraint with orange:** 10% of surface area maximum. It is a signal, not a fill
- **Warm-dark aesthetic:** Public materials use warm cream/off-white `#F7F6F3`, not clinical white
- **No rounded UI:** Chamfer cuts throughout, no `border-radius` except nav pills (8px) and avatar circles

## Stripe system
Two decorative stripes for document and brand use:

**Official document stripe** (vertical, 155×3508px native): For letterheads, right-edge placement. Orange `#FB9800` + cream `#F2E8D5`.

**Public / lanyard stripe** (horizontal, 6143×119px, repeat period ~3071px): For headers, footers, banners, merch. Orange on transparent; works on dark or light.

CSS repeating tile usage:
```css
background: url('assets/reka-pubstripe-tile.svg') repeat-x center / auto 100%;
```

## Motion principles
- Transitions: 120–150ms ease-out for micro, 250–300ms for panel-level
- Spin (HUD mark): 12s linear infinite
- Live dot pulse: 2s ease-in-out infinite (opacity 1→0.25→1)
- Prefer CSS transforms; animate `opacity` and `transform` only
