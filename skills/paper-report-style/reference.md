# Paper report — tokens and structure

Visual-only reference for **Markdown, HTML, Canvas**, and similar docs.

## Fonts

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Archivo:wght@500;600;700&family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500;600&display=swap">
```

## Markdown skeleton (structure only)

```markdown
**EYEBROW** · context · date

# Title

One-line thesis.

| When | Figure | Note |
| --- | --- | --- |
| … | … | … |
| … | … | … |
| … | … | … |

## 01 — Section

Lead paragraph.

> **Callout.** Short decision-relevant note.

### Ledger item — tag
Detail. **Figure**

## Decision
Who / what / next step.
```

## HTML skeleton

Prefer inlining [paper-base.css](paper-base.css) into standalone HTML.

```html
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>…</title>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Archivo:wght@500;600;700&family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500;600&display=swap">
<style>/* paste paper-base.css */</style>
</head>
<body>
<div class="wrap">
  <header>
    <p class="eyebrow"><b>…</b> · … · …</p>
    <h1>…</h1>
    <p class="thesis">…</p>
  </header>
  <div class="band">…</div>
  <section>
    <div class="sechead"><span class="n">01</span><h2>…</h2></div>
    <p class="lede">…</p>
    <div class="callout"><p><b>…</b> …</p></div>
  </section>
  <div class="ledger">…</div>
  <div class="decision">…</div>
</div>
</body>
</html>
```

## Canvas

Paper/ink hierarchy, hairline dividers, orange `--cost` accent for callouts — not purple. Avoid heavy cards.
