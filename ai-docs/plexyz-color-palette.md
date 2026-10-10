# PLExyz — Colour Palette
> Division: Harmonik · Sensing & Digitalization
> Use this file when building any PLExyz UI, marketing, or branded material.

---

## CSS custom properties

```css
:root {
  /* PLExyz / Harmonik purple family */
  --plx-light:    #C8BDE8;   /* light accent / tint */
  --plx-mid:      #865ACE;   /* mid accent */
  --plx-primary:  #6040CC;   /* primary accent — marks, CTAs, highlights */
  --plx-dark:     #281B4F;   /* dark bg / deepest surface */
  --plx-nav:      #241E58;   /* nav sidebar background */
  --plx-on-light: #F7F6F3;   /* content surface behind purple UI */

  /* Active nav state */
  --plx-active-bg:   rgba(96, 64, 204, 0.28);
  --plx-active-text: #A784F1;   /* lightened primary, readable on --plx-nav */
}
```

---

## Full ramp

| Stop | Hex | RGB | CMYK | Use |
|---|---|---|---|---|
| Light tint | `#C8BDE8` | 200, 189, 232 | C14 M19 Y0 K9 | Tinted backgrounds, subtle fills, hover states on light |
| Mid | `#865ACE` | 134, 90, 206 | C35 M56 Y0 K19 | Secondary accents, icon fills, badges |
| **Primary** | `#6040CC` | 96, 64, 204 | C53 M69 Y0 K20 | Main accent — buttons, links, active indicators, marks |
| Dark / bg | `#281B4F` | 40, 27, 79 | C49 M66 Y0 K69 | Deep surface, section background on dark pages |
| Nav sidebar | `#241E58` | 36, 30, 88 | — | Sidebar/nav background in the PLExyz dashboard |

---

## Neutral surfaces used with PLExyz

| Role | Hex | Use |
|---|---|---|
| Content area (light) | `#F7F6F3` | Main page surface behind cards on public-facing pages |
| Panel (light) | `#FFFFFF` | Cards, panels on the light content area |
| Border (light) | `#E5E4E1` | Dividers, card borders on light surface |
| Content area (dark) | `#131318` | Dark-mode dashboard content background |
| Card (dark) | `#1B1B24` | Card / panel surface on dark content |
| Border (dark) | `rgba(255,255,255,0.08)` | Dividers on dark surfaces |

---

## Tested colour combinations

| Foreground | Background | Ratio | Use |
|---|---|---|---|
| `#6040CC` | `#241E58` | — | Active nav item background / sidebar accent |
| `#A784F1` | `#241E58` | ~5:1 | Active nav text on sidebar |
| `#C8BDE8` | `#281B4F` | ~7:1 AA | Body / secondary text on dark purple bg |
| `#FFFFFF` | `#6040CC` | ~5:1 AA | White text on primary purple button |
| `#6040CC` | `#F7F6F3` | 3.8:1 | Purple accent on light surface — use as fill/border, not body text |
| `#281B4F` | `#F7F6F3` | ~13:1 AAA | Dark purple heading text on light page |
| `#F1F1F0` | `#131318` | 18.7:1 AAA | Default body text in dark dashboard |

---

## Inactive nav colour

Derived from mixing the nav sidebar (`#241E58`) with the primary accent:

```
--plx-nav-muted: #7A6E9A   /* tinted muted purple for inactive nav items */
```

```css
.nav-item          { color: #7A6E9A; }
.nav-item:hover    { color: #C8BDE8; }
.nav-item.active   { color: #A784F1; background: rgba(96, 64, 204, 0.28); }
```

---

## Button styles

```css
/* Primary button — purple on white text */
.btn-plx {
  background: #6040CC;
  color: #FFFFFF;
  font-weight: 600;
  clip-path: polygon(7px 0, 100% 0, 100% calc(100% - 7px), calc(100% - 7px) 100%, 0 100%, 0 7px);
}
.btn-plx:hover { background: #865ACE; }

/* Ghost button */
.btn-plx-ghost {
  border: 1px solid #6040CC;
  color: #6040CC;
  background: transparent;
}
.btn-plx-ghost:hover { background: rgba(96, 64, 204, 0.1); }
```

---

## Status and indicator colours

PLExyz dashboards use the standard REKA status palette alongside the purple family:

| Status | Hex | Use |
|---|---|---|
| Healthy / online | `#1AB89C` | Sensor online, zone reporting normally |
| Warning | `#E8A700` | Threshold approached, sensor lag |
| Offline / muted | `#888888` | Sensor offline, zone inactive |
| PLExyz accent | `#6040CC` | Zone density fill, active state |

---

## Dark dashboard surfaces

For the PLExyz dashboard UI:

```css
:root {
  --plx-dash-bg:      #F7F6F3;   /* light content area */
  --plx-dash-panel:   #FFFFFF;   /* cards */
  --plx-dash-border:  #E5E4E1;   /* borders */
  --plx-dash-ink:     #1D1D1D;   /* primary text */
  --plx-dash-ink-2:   #565656;   /* secondary text */
  --plx-dash-ink-3:   #9A9A9A;   /* meta / labels */

  /* sidebar */
  --plx-sidebar-bg:   #241E58;
  --plx-topbar-bg:    #241E58;
  --plx-topbar-border: rgba(96, 64, 204, 0.32);
}
```

---

## Zone density heatmap palette

PLExyz uses a single-hue ramp for occupancy/density visualisation:

| Density | Hex | Opacity | Use |
|---|---|---|---|
| 0–20% | `#6040CC` | 13% | Near-empty |
| 21–40% | `#6040CC` | 29% | Low occupancy |
| 41–60% | `#6040CC` | 50% | Moderate |
| 61–80% | `#6040CC` | 72% | High occupancy |
| 81–100% | `#6040CC` | 93% | Near capacity |

```css
/* Applied as background-color with inline opacity */
.zone { background: #6040CC; }
.zone[data-pct="low"]    { opacity: 0.20; }
.zone[data-pct="mid"]    { opacity: 0.50; }
.zone[data-pct="high"]   { opacity: 0.85; }
```

---

## Typography on PLExyz surfaces

- **Headings on dark purple** (`#281B4F`): `#F1F1F0`
- **Body on dark purple**: `#C8BDE8` (soft light tint, easier on the eyes than stark white)
- **Labels / mono on dark**: `#A784F1` (active text colour)
- **Headings on light** (`#F7F6F3`): `#1D1D1D`
- **Accent text on light**: `#281B4F` (dark purple, high contrast, AAA)

---

## What not to do

- Do not use `#C8BDE8` (light tint) as a button fill — insufficient contrast against white text
- Do not use `#6040CC` as body text on `#F7F6F3` — 3.8:1 fails for small text (fine for large headings 24px+)
- Do not mix PLExyz purple with REKA brand orange as co-equal accents in one UI — pick one to lead
- Do not use the full `#6040CC` purple as a background for large sections — use `#281B4F` or `#241E58`

---

*Source: REKA Brand Guidelines · Harmonik division · PLExyz*
*Almanac: brand-guidelines.html → 03 Colour → Product families*
