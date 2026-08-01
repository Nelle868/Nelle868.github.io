# Nelle868.github.io

# Interactive Portfolio

A single-page personal portfolio built from scratch in **HTML5, CSS3, and JavaScript** — no frameworks, no build step, no dependencies. Everything lives in one `index.html` file and deploys as a static site.

The page is a full-screen "deck": each section fills the viewport and you jump between them one at a time, with a hyperspace-warp transition over an animated galactic starfield.

## Features

- **Galactic background** — a canvas starfield with parallax drift and drifting nebula clouds, rendered on a `<canvas>` behind the content.
- **Hyperspace jump** — scrolling between sections triggers a forward-zoom transition while the stars streak outward from a central burst.
- **Full-page section deck** — one section on screen at a time; a scroll, arrow key, swipe, or side-dot click advances to the next. Sections taller than the viewport scroll internally, then hand off to the next section at their edge.
- **Animated project timeline** — a chronological, month-stamped list of projects with tags and links.
- **Interactive skill carousels** — auto-scrolling rows you can grab, fling, or scrub to speed up.
- **Responsive fallback** — on small screens or without JavaScript, the deck degrades to a normal scrolling page.
- **Accessibility** — respects `prefers-reduced-motion`, keyboard-navigable, semantic HTML.

## Tech Stack

- HTML5
- CSS3 (custom properties, flexbox, grid, keyframe animations, `<canvas>`)
- JavaScript (no libraries)


## Customizing

All colors, fonts, and spacing are driven by CSS custom properties (design tokens) in the `:root` block at the top of the `<style>` tag. Change a value once and it applies everywhere:

```css
:root {
  --font: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --bg:     #050308;   /* deep-space background */
  --accent: #6aa8ff;   /* primary accent */
  --accent-2: #b388ff; /* gradient partner   */
  --jump: 0.44s;       /* hyperspace jump duration */
}
```

To edit content, find the matching `<section>` in the HTML and update the text. Each section is one screen. When adding or removing a section, add or remove its dot in the `.dots` nav in the same position so the indicator stays aligned.
