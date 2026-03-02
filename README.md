# DJuboor.github.io

Personal portfolio site for David N. Juboor, hosted on GitHub Pages.

## Overview

Single-file, self-contained portfolio built with vanilla HTML, CSS, and JS. No build step, no frameworks, no external dependencies beyond Google Fonts (Inter). Features dark/light mode, accordion-based experience and project sections with show all/hide all toggles, and published patent links.

## Quick Start

```bash
# Clone
git clone git@github.com:DJuboor/DJuboor.github.io.git
cd DJuboor.github.io

# Preview locally
open index.html
```

No build tools or local server required — just open `index.html` in a browser.

## Structure

```
.
├── index.html      # Entire site (HTML + CSS + JS, self-contained)
├── .gitignore
└── README.md
```

## Deployment

Pushes to `master` automatically deploy via GitHub Pages.

- **Live URL:** [djuboor.github.io](https://djuboor.github.io)
- **Custom domain:** `davidj.today` (pending DNS configuration)

## Editing Content

All content lives in `index.html`. Sections are marked with HTML comments (`<!-- Experience -->`, `<!-- Patents -->`, etc.) for easy navigation. Each experience/project entry follows this structure:

```html
<div class="entry">
  <button class="entry-trigger" aria-expanded="false">
    <div class="entry-trigger-content">
      <div class="entry-left">
        <span class="entry-title">Company Name</span>
        <span class="entry-role">Role Title</span>
      </div>
    </div>
    <span class="entry-chevron">...</span>
  </button>
  <div class="entry-body">
    <div class="entry-details">
      <ul>
        <li>Accomplishment or detail</li>
      </ul>
    </div>
  </div>
</div>
```

## Design Decisions

- **No frameworks** — single file, zero dependencies, instant load
- **Dark/light mode** — respects `prefers-color-scheme`, persists choice in `localStorage`
- **No dates on experience** — intentional; focuses on what, not when
- **Monochrome palette** — no accent colors, text hierarchy via weight and opacity
- **Inter 400/500** — only two font weights loaded to minimize payload
