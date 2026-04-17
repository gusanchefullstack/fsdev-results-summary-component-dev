# Frontend Mentor — Results Summary Component

A responsive results summary card built from scratch with semantic HTML and modern CSS, solving the [Results Summary Component challenge](https://www.frontendmentor.io/challenges/results-summary-component-CE_K6s0maV) on Frontend Mentor.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-8.0.8-646CFF?style=flat&logo=vite&logoColor=white)
![License](https://img.shields.io/badge/license-ISC-blue)
![Status](https://img.shields.io/badge/status-complete-brightgreen)

## Table of Contents

- [Overview](#overview)
- [Screenshots](#screenshots)
- [Built With](#built-with)
- [Design System](#design-system)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Data Source](#data-source)
- [What I Learned](#what-i-learned)
- [Roadmap](#roadmap)
- [Credits](#credits)
- [License](#license)
- [Author](#author)

## Overview

This project implements a pixel-accurate, accessible, and fully responsive results summary component using only HTML and CSS — no frameworks, no JavaScript libraries. The layout adapts fluidly from 320px mobile screens up to large desktop widths, using a mobile-first workflow and CSS custom properties for every color, gradient, and typographic token.

Users should be able to:

- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page

## Screenshots

| Desktop | Mobile |
|---------|--------|
| ![Desktop design](./design/desktop-design.jpg) | ![Mobile design](./design/mobile-design.jpg) |

## Built With

- Semantic HTML5 markup
- CSS custom properties (design tokens in `variables.css`)
- Flexbox & CSS Grid
- BEM-style class naming
- Mobile-first responsive workflow
- [Vite 8.0.8](https://vite.dev/) — dev server and production build
- Hanken Grotesk — self-hosted local font files (weights 500, 700, 800)

## Design System

All design tokens are parameterized in [`src/styles/variables.css`](./src/styles/variables.css) so the theme can be changed in one place.

### Primary Colors

| Token | Value |
|-------|-------|
| Light red | `hsl(0, 100%, 67%)` |
| Orangey yellow | `hsl(39, 100%, 56%)` |
| Green teal | `hsl(166, 100%, 37%)` |
| Cobalt blue | `hsl(234, 85%, 45%)` |

### Gradients

| Token | Value |
|-------|-------|
| Background (top) | `hsl(252, 100%, 67%)` → `hsl(241, 81%, 54%)` |
| Score circle | `hsla(256, 72%, 46%, 1)` → `hsla(241, 72%, 46%, 0)` |

### Typography

- Family: **Hanken Grotesk**
- Weights: **500**, **700**, **800**
- Base body size: **18px**

## Installation

### Prerequisites

- Node.js **>= 18**
- npm **>= 9**

### Setup

```bash
# Clone the repo
git clone https://github.com/gusanchefullstack/fsdev-results-summary-component-dev.git
cd fsdev-results-summary-component-dev

# Install dependencies
npm install
```

## Usage

```bash
# Start the Vite dev server (http://localhost:5173)
npm run dev

# Build for production (outputs to ./dist)
npm run build

# Preview the production build locally
npm run preview
```

## Project Structure

```
fsdev-results-summary-component-dev/
├── assets/
│   ├── fonts/             # Self-hosted Hanken Grotesk font files
│   └── images/            # Category icons (SVG) and favicon
├── design/                # Reference screenshots (mobile, desktop, active-states)
├── src/
│   ├── index.html         # Application entry point
│   └── styles/
│       ├── variables.css  # Design tokens: colors, gradients, typography
│       └── main.css       # Layout and component styles
├── data.json              # Source data for the four score categories
├── style-guide.md         # Challenge style guide
├── vite.config.js         # Vite config (root: src, publicDir: ../assets)
└── package.json
```

## Data Source

Category scores are driven by [`data.json`](./data.json):

```json
[
  { "category": "Reaction", "score": 80, "icon": "./assets/images/icon-reaction.svg" },
  { "category": "Memory",   "score": 92, "icon": "./assets/images/icon-memory.svg" },
  { "category": "Verbal",   "score": 61, "icon": "./assets/images/icon-verbal.svg" },
  { "category": "Visual",   "score": 72, "icon": "./assets/images/icon-visual.svg" }
]
```

## What I Learned

Key topics reinforced while building this component:

- **CSS custom properties as a single source of truth** — keeping every color, gradient, and font token in `variables.css` means theming is a one-file change. [MDN: Using CSS custom properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties).
- **Mobile-first responsive layout** — starting at 320px and scaling up with `min-width` media queries prevents desktop-first override spaghetti.
- **Flexbox vs. Grid decisions** — Grid for the two-panel card layout (stacks on mobile, side-by-side on desktop); Flexbox for the per-row score items.
- **Self-hosting fonts** — using `@font-face` with local `.woff2` files avoids a render-blocking request to Google Fonts and removes a third-party dependency.
- **Vite with a nested `src/` root** — configuring `root: 'src'` and `publicDir: '../assets'` lets source code live in `src/` while keeping shared assets at the project root.
- **Accessibility defaults** — semantic landmarks (`<main>`, `<section>`, `<h1>`, `<ul>`), meaningful `alt` text, and visible focus states on the call-to-action.
- **BEM naming** — `summary__item--reaction` style modifiers keep variant styling predictable without utility-class sprawl.

## Roadmap

- [x] Semantic HTML structure
- [x] Design tokens in CSS custom properties
- [x] Mobile-first responsive layout (mobile + desktop)
- [x] Tablet breakpoint inferred between mobile and desktop
- [x] Hover and focus states for the Continue button
- [x] Self-hosted Hanken Grotesk fonts
- [ ] Render category rows dynamically from `data.json`
- [ ] Lighthouse accessibility pass (target: 100)
- [ ] Deploy preview to GitHub Pages / Vercel

## Credits

- Challenge and design assets by [Frontend Mentor](https://www.frontendmentor.io/).
- Font family [Hanken Grotesk](https://fonts.google.com/specimen/Hanken+Grotesk) by Alfredo Marco Pradil.
- Planning, implementation, and incremental commit structure assisted by **Claude Code** (Opus 4.7).

## License

Distributed under the ISC License. See [`package.json`](./package.json) for details.

## Author

**Gustavo Sanchez Galarza**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gustavosanchezgalarza/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/gusanchefullstack)
[![Hashnode](https://img.shields.io/badge/Hashnode-2962FF?style=for-the-badge&logo=hashnode&logoColor=white)](https://hashnode.com/@gusanchedev)
[![X](https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/gusanchedev)
[![Bluesky](https://img.shields.io/badge/Bluesky-0085FF?style=for-the-badge&logo=bluesky&logoColor=white)](https://bsky.app/profile/gusanchedev.bsky.social)
[![freeCodeCamp](https://img.shields.io/badge/freeCodeCamp-0A0A23?style=for-the-badge&logo=freecodecamp&logoColor=white)](https://www.freecodecamp.org/gusanchedev)
[![Frontend Mentor](https://img.shields.io/badge/Frontend_Mentor-3F54A3?style=for-the-badge&logo=frontendmentor&logoColor=white)](https://www.frontendmentor.io/profile/gusanchefullstack)
