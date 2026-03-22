# Presentation figures

Put screenshot files here and name them by **figure number**, for example:

- `fig1.png`
- `fig2.jpg`
- `fig12.png`

Supported extensions: `.png`, `.jpg`, `.jpeg`, `.webp`, `.gif` (use whatever matches your export).

## How to wire them in `index.html`

Paths are relative to the project root, e.g. `figures/fig3.png`.

### One image on a slide

On the slide’s `.image-column`, keep:

`class="image-column slide-figures slide-figures--1"`

Replace the dashed **placeholder** block with a real image:

```html
<div class="slide-figure-frame">
	<img src="figures/fig7.png" alt="Figure 7" />
</div>
```

Optional caption under the image:

```html
<p class="slide-figure-caption">Figure 7 — Descriptives dialog</p>
```

### Two images (stacked top → bottom)

Use:

`class="image-column slide-figures slide-figures--stack-2"`

Two `<figure class="slide-figure-block">` children (or placeholders). Order = top first, then below.

### Three images (pyramid: one on top, two below side by side)

Use:

`class="image-column slide-figures slide-figures--pyramid"`

Three `<figure class="slide-figure-block">` children **in order**: (1) top row, (2) bottom left, (3) bottom right.

### Other stacked layouts

`slide-figures--stack` — generic vertical stack with tighter max-heights.

---

When you send which figure number belongs to which slide, the mapping can be applied by updating `src="figures/figN…"` (and layout class on `.image-column` if a slide needs 2+ images).
