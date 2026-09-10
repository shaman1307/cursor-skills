---
name: paper-report-style
description: >-
  Visual system for standalone HTML documentation and briefings: Archivo +
  IBM Plex typography, paper/ink palette, KPI band, chart boxes, ledger rows,
  folds, decision/callout accents. Use when creating documentation HTML,
  status/briefing pages, or styled analytical write-ups — appearance only.
---

# Paper report visual system

Apply this **look and layout chrome** when producing documentation HTML or similarly styled briefings. This skill is about **typography, color, spacing, and UI chrome** — not about what to say.

Read [reference.md](reference.md) and reuse [paper-base.css](paper-base.css).

## Typography

| Role | Font |
|---|---|
| Body | IBM Plex Sans 400/500/600 · 15px · line-height 1.55 |
| Display (`h1`–`h3`, large figures) | Archivo 500/600/700 |
| Labels, tags, deltas, table headers, tooltips | IBM Plex Mono · uppercase · tracking ~0.09–0.13em · tabular nums |

Google Fonts:

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Archivo:wght@500;600;700&family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500;600&display=swap">
```

## Color tokens

| Token | Light | Dark |
|---|---|---|
| `--paper` | `#EFF2F1` | `#0F1413` |
| `--surface` | `#FAFBFA` | `#161B1A` |
| `--surface-2` | `#E7EBEA` | `#1E2523` |
| `--ink` | `#141A1C` | `#E7EBE9` |
| `--ink-2` | `#3C4749` | `#BAC3C1` |
| `--ink-3` | `#667172` | `#8E9997` |
| `--rule` / `--rule-2` | `#D2D8D7` / `#BFC7C6` | `#2A3230` / `#3A4341` |
| `--cost` (accent / inflight) | `#C2661B` | `#CC7429` |
| `--rel` / `--realized` | `#0E8F73` | `#20A18C` |
| `--fleet` | `#3A6FD8` | `#5B90E8` |
| `--block` | `#9C3587` | `#E86FA8` |
| `--notstarted` | `#667172` | `#8E9997` |

Support `data-theme="light|dark"` and `prefers-color-scheme`. Soft fills: `--*-soft` rgba variants in CSS.

## Layout chrome

- Max width **1080px**; page padding `40px 28px 72px`
- Hairline borders (`--rule`), **not** drop shadows
- Radius **2–4px** only
- Decision / callout: **3px left accent** in `--cost`
- Print: force light palette, A4 landscape; hide tips and column toggles

## UI components (classes)

Use the CSS class names from `paper-base.css`:

- `.wrap` · `.eyebrow` · `header` · `.thesis`
- `.band` (3 KPI columns) · `.fig` · `.delta` · `.when` · `.perdm` · `.sub`
- `.sechead` · `.n` · `.period` · `.lede`
- `.chartbox` · `.legend` · `.swatch` · `.tip` · `.tlkey` · `.flag` · `.bandkey`
- `.ledger` · `.item` · `.pip` · `.tag` · `.crew`
- `.fold` / `summary` · `.decision` · `.settled` · `.callout`
- `table` · `.coltoggle` · `.mono` · `td.spark`

Status accent classes (color only): `.r` realized · `.i` inflight · `.q` fleet · `.x` blocked · `.n` notstarted  
Crew: `.crew` dashed; `.crew.dep` solid border.

## Anti-patterns

```text
❌ Inter / Roboto / system-ui as primary stack
❌ Purple / indigo marketing gradients
❌ Heavy card shadows, large radius, pill chrome
❌ Overriding this look inside product app UI unless asked
```
