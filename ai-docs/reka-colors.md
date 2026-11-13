# REKA Colour System
> Complete colour reference for generating on-brand UI, documents, and visuals.
> Updated: June 2026

## Primary orange (the brand)
| Token | Hex | RGB | CMYK | Use |
|---|---|---|---|---|
| Brand orange | `#FB9800` | 251, 152, 0 | C0 M39 Y100 K2 | Marks, fills, primary actions. The one official orange. |
| Highlight | `#FFB23E` | 255, 178, 62 | C0 M30 Y76 K0 | Glow / lighter accent on dark surfaces |
| Secondary | `#E65D01` | 230, 93, 1 | C0 M60 Y100 K10 | Hover state; dark end of orange gradients |

**Rule:** `#FB9800` is the only brand orange. `#f7941d`, `#E8742A`, `#FFA910` are retired.

## Surface modes
### Public (light-first, default)
| Token | Hex | Use |
|---|---|---|
| Background | `#F7F6F3` | Primary content surface |
| Panel | `#FFFFFF` | Cards, panels |
| Line | `#E5E4E1` | Borders, dividers |
| Ink | `#1D1D1D` | Primary text |
| Ink 2 | `#565656` | Secondary text |
| Ink 3 | `#9A9A9A` | Captions, meta |

### Internal (dark, for internal tools and brand kit)
| Token | Hex | Use |
|---|---|---|
| Near-black | `#0B0B0C` | Primary surface |
| Surface | `#161618` | Cards, panels |
| Surface 2 | `#1D1D20` | Raised elements |
| Ink | `#F1F1F0` | Primary text on dark |
| Ink 2 | `#B9B9BD` | Secondary text on dark |
| Mute | `#76767C` | Captions on dark |

## Product family palettes

### Harmonik / PLExyz (purple)
| Stop | Hex | Use |
|---|---|---|
| Light accent | `#C8BDE8` | Backgrounds, tints |
| Mid | `#865ACE` | Secondary accents |
| Primary *(TBC)* | `#6040CC` | Main accent — placeholder, confirm hex |
| Dark / bg | `#281B4F` | Dark surface, sidebar dark |

### Kinetik / OVERride (teal)
| Stop | Hex | Use |
|---|---|---|
| Light tint | `#BAE4E1` | Backgrounds |
| Mid | `#6AD1BF` | Secondary accents |
| Primary *(TBC)* | `#1AB89C` | Main accent — placeholder, confirm hex |
| Dark / sidebar | `#063028` | Dark nav sidebar |

### Heuristik / AntaraX (blue)
| Stop | Hex | Use |
|---|---|---|
| Light accent | `#6AAEFF` | Backgrounds, tints |
| Mid | `#0496FF` | Secondary accents |
| Primary | `#1268F7` | Main accent |
| Dark / bg | `#16366B` | Dark surface |
| Sidebar dark | `#0D2850` | Nav sidebar |

### Esoterik / Tinara (maroon)
| Stop | Hex | Use |
|---|---|---|
| Light tint | `#CAB9C7` | Backgrounds |
| Mid | `#8D6885` | Secondary accents |
| Primary | `#501643` | Main accent |
| Dark / sidebar | `#2D0A22` | Dark nav sidebar |

## States, tints and surface steps (tokens 1.1.0, 13 November 2026)
For interfaces and documents that show a state. Each text colour is checked against its own tint (WCAG AA or better). Not for marketing colour.

| Token | Light | Dark | Use |
|---|---|---|---|
| Error | `#B42318` | `#F7867C` | Text and icons for a fault (5.8:1 and 7.1:1 on the tint) |
| Error tint | `#FEECEB` | `#2E1312` | Behind an error message |
| Success | `#067647` | `#5FD49A` | Text and icons for done (5.2:1 and 8.4:1) |
| Success tint | `#E7F8EF` | `#10291C` | Behind a success message |
| Warning | `#B54708` | `#F7B15A` | Icons and strokes for attention; dark text on its tint 8.9:1 |
| Warning tint | `#FEF4E6` | `#2B1D0A` | Behind a warning |
| Warning ink | `#93370D` | (Warning) | Text on the light warning tint (6.9:1) |
| Orange tint | `#FFF2DF` | `#2A1E0B` | The key path and highlighted rows (the light value is reka.re's) |
| Orange tint ink | `#6B3F00` | `#FFC46B` | Text on the orange tint (8.1:1 and 10.4:1) |

| Surface step | Light | Dark |
|---|---|---|
| Sunken | (Background) | `#131315` |
| Surface 1 | `#FBFAF8` | (Surface) |
| Surface 2 | `#F2F0EB` | (Surface 2) |
| Surface 3 | `#EFEDE8` | `#232327` |
| Surface 4 | `#E4E1D9` | `#2C2C31` |
| Outline | `#8A8A90` (3.2:1, for controls) | (Mute) |

## Secondary / internal colours
| Name | Hex | Use |
|---|---|---|
| REKA Products | `#274677` | Tagging product documents internally |
| REKA Services | `#501643` | Tagging service documents internally |
| External | `#FFFFFF` | External-facing white |
| Internal | `#0B0B0C` | Internal-facing black |

## Accent libraries (illustration / graphics only — not UI)
### Bold neon
`#00B3FF` · `#00F0FF` · `#3B72FF` · `#FF5689` · `#FF5757` · `#FF7A00`

### Soft pastel
`#ABC1F9` · `#CBE2F7` · `#ABE1F8` · `#A6F3F8` · `#F8CEDA` · `#F9B6B6` · `#F7DCC4`

## Retired (do not use)
`#f7941d` · `#E07D10` · `#E8742A` · `#0062FB` (all superseded by `#FB9800` or family colours)

## Contrast / accessibility
- `#FB9800` on `#0B0B0C` → 8.4:1 (AAA) ✓ — use freely on dark
- `#FB9800` on `#FFFFFF` → 2.4:1 (Fail for text) — use as fill/icon only on light
- For amber inline text on light, darken the orange or use the secondary `#E65D01`
