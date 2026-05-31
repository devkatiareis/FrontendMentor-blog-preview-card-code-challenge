# Front-end Style Guide - Blog Preview Card

This document details the design specifications, variables, and typography implemented in the final CSS of the project.

## 🛠️ Structural and Visual Analysis

The central component was built using the following web development techniques:

* **Neo-Brutalist Shadow:** The card does not use soft shadows (`box-shadow` with blur). Instead, it displays a solid black border offset to the right and down, creating a rigid, high-contrast 3D effect.

* **Rounded Corners:** Application of a moderate `border-radius` both on the main card, the top image, and the yellow badge.

* **Typography and Hierarchy:** Use of sans-serif fonts with strong weight variations (bold on the title and author's name) to guide the user's gaze.

* **Responsive Layout:** Structured with Flexbox CSS to perfectly align the spacing (padding) between the image, texts, and the author's footer.

## 🎨 Color Palette and Style

* **Vibrant Background:** The use of solid yellow (`#f4d04e`) saturates the screen and highlights the central white component.

* **High Contrast:** Purely black and white elements generate excellent readability, meeting web accessibility best practices.


## Layout & Responsiveness

The component is engineered with a mobile-first design workflow and supports seamless responsiveness.

- **Mobile Viewport (Design Target):** 375px
- **Desktop Viewport (Design Target):** 1440px
- **Max Component Width:** 384px (Optimized `.card` container)

> 💡 **Responsiveness & A11y:** Spacings and dimensions adapt properly across all viewports starting from 320px up to ultra-wide displays using Flexbox layouts, meeting WCAG requirements.

---

## Colors

These are the design colors mapped to CSS Custom Properties (`:root`) used throughout the project.

### Theme Colors

- **Vibrant Yellow (Primary Background):** `#f4d04e` (`--color-primary`)
- **Dark Yellow (Secondary Accent):** `#CFA200` (`--color-secondary`)
- **Pure White (Card Background):** `#ffffff` (`--color-white`)

### Neutral Shades

- **Dark Charcoal (Text, Borders & Shadows):** `#111111` (`--color-grey-pure`)
- **Medium Gray (Body Copy & Subtitles):** `#6B6B6B` (`--color-grey-medium`)

### Accessibility & Utilities

- **High-Contrast Blue (Keyboard Focus Ring):** `#005fcc` (`--color-focus-outline`)
- **Accessible Dark Blue (Footer Links Contrast):** `#1a2eb3` (`--color-link-dark`)

---

## Typography

### Font Family

- **Main Font:** [Figtree](https://fonts.google.com/specimen/Figtree?preview.script=Latn) (`sans-serif`)

### Font Sizes & Weights

- **Card Heading (`.card-title`):** 24px | Weight: 800 (Extra Bold) | Line Height: 1.3
- **Description Paragraph (`.post-excerpt`):** 16px | Weight: 500 (Medium) | Line Height: 1.5
- **Meta Info (`.badge`, `.publish-date`, `.author-name`):** 14px | Weights: 500 & 800
- **Attribution Footer (`.attribution`):** 12px (0.75rem) | Weight: 700 (Links)

---

## Interactive Component Specifications

### 1. Neo-Brutalist Shadow Effect

The signature flat 3D look is created via solid borders and zero-blur offset box shadows:
- **Default State:** `border: 1px solid #111111; box-shadow: 8px 8px 0px 0px #111111;`
- **Hover State:** Card translates diagonally via `transform: translate(-4px, -4px);` and shifts the shadow to `12px 12px 0px 0px #111111;`.

### 2. Focus Indicator Requirements

To guarantee full keyboard navigation accessibility, default browser focus rings are suppressed on interactive items (`.card-title-link` and `.attribution a`). They are replaced by a custom focus state:
- **Selector:** `:focus-visible`
- **Outline:** `3px solid #005fcc` with an `outline-offset` of `4px`.
