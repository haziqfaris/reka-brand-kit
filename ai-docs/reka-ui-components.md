# REKA UI Components — Dashboard Specification
> Use this to generate on-brand dashboards, admin panels, and data UIs.
> Updated: June 2026

## Layout structure
```
┌─────────────────────────────────────────────────────────────────┐
│ Browser chrome (dark #1C1C20, dots + family favicon)            │
├──────────────────────────────────────────────────────────────────┤
│  SIDEBAR (192px)     │  TOPBAR (54px, dark family)               │
│  family dark bg      │  Page title (bold white) + division label │
│                      ├───────────────────────────────────────────┤
│  [logo + name]       │  STATUS STRIP (24px, accent-tinted)       │
│  [section label]     ├───────────────────────────────────────────┤
│  [nav items]         │  KPI CARDS (4 × 1/4 width)                │
│  ...                 ├───────────────────────────────────────────┤
│  [section label]     │  HERO PANEL (65%)  │  SIDE COL (35%)      │
│  [nav items]         │  product hero viz  │  panel 1             │
│                      │                    │  panel 2             │
│  [profile card]      │                    │                      │
│  [settings]          │                    │                      │
└──────────────────────────────────────────────────────────────────┘
```

## Sidebar
```css
width: 192px;
background: [family dark hex]; /* e.g. #241E58 for PLExyz */
border-right: 1px solid rgba(accent, 0.2);
```

**Brand header:**
```html
<div style="display:flex;align-items:center;gap:10px;padding:14px 13px 13px;border-bottom:1px solid rgba(accent,0.2)">
  <div style="width:22px;height:22px;background:[accent];clip-path:polygon(0 0,72% 0,100% 28%,100% 100%,0 100%)"></div>
  <span style="font-weight:700;color:#F1F1F0">[Product name]</span>
</div>
```

**Nav section labels:**
```css
font-family: 'JetBrains Mono'; font-size: 0.54rem; letter-spacing: 0.16em;
text-transform: uppercase; color: rgba(accent, 0.35); padding: 10px 12px 4px;
```

**Nav items:**
```css
.nav-item {
  display: flex; align-items: center; gap: 9px;
  padding: 8px 10px; font-size: 0.77rem;
  border-radius: 8px; /* rounds for nav pills */
  color: [nav_muted]; /* tinted inactive color */
}
.nav-item.active {
  color: #FFFFFF; font-weight: 600;
  background: rgba(accent, 0.28);
}
```

**Profile card (sidebar bottom):**
```html
<div style="border-top:1px solid rgba(accent,0.15);padding:10px 12px;display:flex;align-items:center;gap:9px">
  <div style="width:28px;height:28px;border-radius:50%;background:rgba(accent,0.28);border:1.5px solid rgba(accent,0.45);display:flex;align-items:center;justify-content:center;color:#FFF;font-size:.72rem;font-weight:700">U</div>
  <div>
    <div style="font-size:.76rem;font-weight:600;color:#F1F1F0">User Name</div>
    <div style="font-size:.62rem;color:[nav_muted]">Role · Product</div>
  </div>
</div>
```

## Topbar
```css
height: 54px; background: [family dark hex]; /* same as sidebar */
border-bottom: 2px solid rgba(accent, 0.28);
display: flex; align-items: center; justify-content: space-between; padding: 0 18px;
```

**Left (title + description):**
```html
<div>
  <div style="font-size:.95rem;font-weight:700;color:#FFF">[Page title]</div>
  <div style="font-size:.68rem;color:rgba(accent,0.55)">[Division · Remit]</div>
</div>
```

**Right (live indicator + bell):**
```html
<div style="display:flex;align-items:center;gap:10px">
  <span style="display:flex;align-items:center;gap:4px;font-family:'JetBrains Mono';font-size:.58rem;color:rgba(accent,0.45)">
    <span style="width:5px;height:5px;border-radius:50%;background:[accent];animation:pulse 2s infinite"></span>LIVE
  </span>
  [bell icon]
</div>
```

## Status strip
```css
height: 24px; background: rgba(accent, 0.04);
border-bottom: 1px solid rgba(accent, 0.12);
display: flex; align-items: center; gap: 16px; padding: 0 18px;
font-family: 'JetBrains Mono'; font-size: 0.60rem;
```

## KPI cards
```css
/* Four cards, equal width */
.kpi {
  padding: 10px 12px;
  background: #FFFFFF; /* or #1B1B24 on dark */
  border: 1px solid #E5E4E1;
  clip-path: polygon(7px 0, calc(100% - 7px) 0, 100% 7px, 100% calc(100% - 7px),
                     calc(100% - 7px) 100%, 7px 100%, 0 calc(100% - 7px), 0 7px);
}
.kpi.hero { border-top: 2px solid [accent]; } /* first/primary metric */
.kpi-label { font-family:'JetBrains Mono'; font-size:.63rem; letter-spacing:.09em; text-transform:uppercase; color:[ink3]; }
.kpi-value { font-family:'JetBrains Mono'; font-size:1.65rem; font-weight:600; letter-spacing:-.04em; line-height:1; }
.kpi-sub   { font-size:.62rem; color:[accent]; font-weight:500; margin-top:4px; }
/* Sparkline: 80×26px SVG at right edge */
```

## Panels — chamfer polygon
```css
/* Hero panel */
clip-path: polygon(12px 0, calc(100% - 12px) 0, 100% 12px, 100% calc(100% - 12px),
                   calc(100% - 12px) 100%, 12px 100%, 0 calc(100% - 12px), 0 12px);

/* Side panels */
clip-path: polygon(9px 0, calc(100% - 9px) 0, 100% 9px, 100% calc(100% - 9px),
                   calc(100% - 9px) 100%, 9px 100%, 0 calc(100% - 9px), 0 9px);
```

## Status list (side panel)
```html
<div style="display:flex;align-items:center;gap:9px;padding:7px 0;border-bottom:1px solid [br];font-size:.77rem">
  <span style="width:7px;height:7px;border-radius:50%;background:[status-color];flex:none"></span>
  <span style="font-weight:500">[Label]</span>
  <span style="margin-left:auto;font-family:'JetBrains Mono';font-size:.62rem;opacity:.55">[Value]</span>
</div>
```
Status colours: OK `#1AB89C` · Warning `#E8A700` · Muted/offline `#888`

## Bar list (side panel)
```html
<div>
  <div style="display:flex;justify-content:space-between;font-size:.73rem;margin-bottom:4px">
    <span>[Label]</span><b style="font-family:'JetBrains Mono';font-size:.68rem">[pct]%</b>
  </div>
  <div style="height:4px;background:rgba(accent,0.15);overflow:hidden;clip-path:polygon(0 0,calc(100% - 3px) 0,100% 3px,100% 100%,0 100%)">
    <div style="height:100%;background:[accent];width:[pct]%;opacity:.9"></div>
  </div>
</div>
```

## Light/dark surface selection
| Context | Mode |
|---|---|
| Public website, client portal, product dashboards | Light — `#F7F6F3` |
| Internal tools, operations consoles, brand kit | Dark — `#131318` |
| Immersive sections / hero zones (public) | Dark allowed for dramatic effect |
| Sidebar + topbar | Always dark (family dark bg) regardless of content mode |

## CSS animation: live pulse
```css
@keyframes pulse {
  0%, 100% { opacity: 1; }
  50%       { opacity: 0.25; }
}
```
