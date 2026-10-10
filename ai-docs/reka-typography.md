# REKA Typography
> Type specification for UI, documents, and marketing materials.
> Updated: June 2026

## Two typefaces only
| Family | Role | Source |
|---|---|---|
| **Poppins** | Display, headings, UI labels, body | Google Fonts |
| **JetBrains Mono** | Data, figures, labels, telemetry, code | Google Fonts |

**Never substitute decorative or system fonts in brand materials.**

## Poppins weights
- 300 — Light (rarely, for super-large display only)
- 400 — Body, descriptions
- 500 — UI labels, sub-headings  
- 600 — Section headings
- 700 — Primary headings
- 800 — Hero / cover display text

## JetBrains Mono weights
- 400 — Data tables, code
- 500 — Labels, captions (most common)
- 700 — Bold data callouts

## Type scale
| Name | Size | Weight | Line-height | Use |
|---|---|---|---|---|
| Hero | clamp(2.4rem, 4vw, 4rem) | 800 | 1.0 | Cover headlines |
| H1 | clamp(2rem, 3vw, 3rem) | 700 | 1.05 | Page titles |
| H2 | clamp(1.5rem, 2vw, 2.2rem) | 700 | 1.1 | Section headings |
| H3 | 1.3rem | 600 | 1.2 | Sub-section headings |
| H4 | 1rem | 600 | 1.3 | Card/panel headings |
| Body | 0.95–1rem | 400 | 1.55–1.6 | Paragraphs |
| Small | 0.8–0.88rem | 400 | 1.5 | Descriptions, meta |
| Label | 0.62–0.72rem | 500 | 1 | Mono UI labels (uppercase, tracked 0.08–0.14em) |
| Data | 1.5–2rem | 600–700 | 1 | KPI values (JetBrains Mono) |

## Usage rules
- Poppins 600–700 for headings; 400 for body
- JetBrains Mono for labels, figures, code and telemetry — uppercase, letter-spacing 0.08–0.14em
- Body text at 15–17px, line-height 1.55–1.6
- Keep measure under ~70 characters per line
- Never use Poppins below weight 300

## Import (Google Fonts)
```html
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">
```

## CSS variables
```css
:root {
  --ui:   'Poppins', system-ui, sans-serif;
  --mono: 'JetBrains Mono', ui-monospace, monospace;
}
```
