# Paper report — tokens, CSS, skeleton

Visual-only reference. Prefer inlining [paper-base.css](paper-base.css) into standalone HTML.

## Fonts

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Archivo:wght@500;600;700&family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500;600&display=swap">
```

## Skeleton (structure chrome only)

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

  <div class="band">
    <div>
      <p class="when">…</p>
      <p class="fig peak">…<span class="unit">…</span></p>
      <p class="perdm">…</p>
      <p class="sub">…</p>
    </div>
    <div>
      <p class="when">…</p>
      <p class="fig now">…</p>
      <span class="delta">…</span>
    </div>
    <div>
      <p class="when">…</p>
      <p class="fig fwd">…</p>
    </div>
  </div>

  <details class="fold">
    <summary><span class="ftxt">…</span><span class="fhint">…</span></summary>
    <div class="foldbody">…</div>
  </details>

  <section>
    <div class="sechead"><span class="n">01</span><h2>…</h2><span class="period">…</span></div>
    <p class="lede">…</p>
    <figure>
      <div class="legend"><span><i class="swatch" style="background:var(--cost)"></i> …</span></div>
      <div class="chartbox">…</div>
      <figcaption>…</figcaption>
    </figure>
    <div class="callout"><p><b>…</b> …</p></div>
  </section>

  <div class="ledger">
    <div class="item">
      <div class="pip r"></div>
      <div class="what"><h3>… <span class="tag r">…</span></h3><p>…</p></div>
      <div class="num"><strong class="r">…</strong>…</div>
    </div>
  </div>

  <div class="decision">
    <p class="who">…</p>
    <h3>…</h3>
    <p>…</p>
  </div>

  <footer>…</footer>
</div>
</body>
</html>
```

## Canvas mapping

When using Cursor Canvas instead of HTML: paper/ink hierarchy, hairline dividers, orange `--cost` accent for callouts — not purple. Avoid heavy cards.
