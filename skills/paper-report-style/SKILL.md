---
name: paper-report-style
description: >-
  Visual system for documentation and briefings (Markdown, HTML, Canvas, and
  similar): Archivo + IBM Plex typography, paper/ink palette, KPI band, ledger
  rows, decision/callout accents. Use when creating docs, status/briefings, or
  styled analytical write-ups — appearance only, any common doc format.
---

# Paper report visual system

Apply this **look and layout chrome** when producing documentation — **Markdown, HTML, Canvas, or similar**. This skill is about **typography, color, spacing, and structure** — not about what to say.

Read [reference.md](reference.md). For standalone HTML, reuse [paper-base.css](paper-base.css). For Markdown and other formats, match the same hierarchy and tokens (see below).

## Typography

| Role | Font / treatment |
|---|---|
| Body | IBM Plex Sans 400/500/600 · ~15px · line-height 1.55 |
| Display (`h1`–`h3`, large figures) | Archivo 500/600/700 |
| Labels, tags, deltas, table headers | IBM Plex Mono · uppercase · tracking ~0.09–0.13em · tabular nums |

When the format cannot load webfonts (plain `.md` in git), keep the **roles**: short mono-style eyebrow/labels, strong display title, calm body — do not switch to Inter/Roboto/system marketing stacks in HTML/CSS targets.

Google Fonts (HTML / rich preview):

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

## Layout chrome (all formats)

Document structure pattern:

1. Mono eyebrow (context · date · scope)
2. Strong title
3. One-line thesis
4. Optional 3-column KPI band
5. Numbered section heads (`01` / `02` …)
6. Callouts with left accent (cost/orange)
7. Optional ledger rows and decision block

Shared constraints:

- Max content width ~**1080px** when layout is controlled
- Hairline dividers, **not** drop shadows
- Radius **2–4px** only (when CSS applies)
- No purple/indigo marketing gradients; no heavy cards

## Format notes

| Format | How to apply |
|---|---|
| **HTML** | Inline/link `paper-base.css`; use class names below |
| **Markdown** | Same section order and hierarchy; tables for KPI/ledger; blockquotes or `>` for callouts; no inventing fake CSS in `.md` |
| **Canvas / rich UI** | Paper/ink hierarchy, hairline rules, `--cost` accent — not purple |

## HTML classes (`paper-base.css`)

- `.wrap` · `.eyebrow` · `header` · `.thesis`
- `.band` · `.fig` · `.delta` · `.when` · `.perdm` · `.sub`
- `.sechead` · `.n` · `.period` · `.lede`
- `.chartbox` · `.legend` · `.swatch` · `.tip` · `.tlkey` · `.flag` · `.bandkey`
- `.ledger` · `.item` · `.pip` · `.tag` · `.crew`
- `.fold` / `summary` · `.decision` · `.settled` · `.callout`
- `table` · `.coltoggle` · `.mono` · `td.spark`

Status accents: `.r` realized · `.i` inflight · `.q` fleet · `.x` blocked · `.n` notstarted

## Anti-patterns

```text
❌ Inter / Roboto / system-ui as primary stack (where fonts are controllable)
❌ Purple / indigo marketing gradients
❌ Heavy card shadows, large radius, pill chrome
❌ Treating this skill as HTML-only
❌ Overriding this look inside product app UI unless asked
```
