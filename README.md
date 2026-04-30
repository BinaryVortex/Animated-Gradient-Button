# Animated Gradient Button

A minimal, dependency-free animated gradient button built with pure HTML and CSS. Perfect for CTAs, landing pages, and UI experiments — easy to customize and accessible by default.

![Animated Gradient Button Screenshot](./Screenshot%202024-05-30%20214310.png)

Demo
- Open the included `index.html` in your browser to see the button in action.
- (Optional) Host on GitHub Pages or any static host for a live demo.

Why this project
- Minimal: no JavaScript required.
- Customizable: colors, speed, size and shape are controlled via CSS variables.
- Lightweight: pure HTML + CSS — great for learning and production use.

Features
- Smooth gradient animation across the button surface.
- Hover & focus states with accessible focus outline.
- Easy to customize via CSS variables.
- Works across modern browsers.

Quick start
1. Clone the repo:
   git clone https://github.com/BinaryVortex/Animated-Gradient-Button.git
2. Open `index.html` in your browser, or integrate the HTML/CSS into your site.

Basic usage
Add the markup:

```html
<button class="ag-button">Click me</button>
```

Include the CSS (example — the repo contains the full implementation in styles.css):

```css
.ag-button{
  --ag-padding: 12px 28px;
  --ag-radius: 10px;
  --ag-speed: 3s;
  --ag-color-a: #ff7a18;
  --ag-color-b: #af002d;
  --ag-color-c: #33001b;

  display: inline-block;
  padding: var(--ag-padding);
  border-radius: var(--ag-radius);
  border: 0;
  color: #fff;
  font-weight: 600;
  cursor: pointer;
  position: relative;
  background: linear-gradient(90deg, var(--ag-color-a), var(--ag-color-b), var(--ag-color-c));
  background-size: 300% 300%;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
  animation: ag-animate var(--ag-speed) linear infinite;
  box-shadow: 0 6px 18px rgba(0,0,0,0.2);
}

.ag-button:hover{ transform: translateY(-2px); }

@keyframes ag-animate{
  0%{ background-position: 0% 50%; }
  50%{ background-position: 100% 50%; }
  100%{ background-position: 0% 50%; }
}

/* Show a clear focus ring for accessibility */
.ag-button:focus{
  outline: 3px solid rgba(255,255,255,0.25);
  outline-offset: 3px;
}
```

Customization
- Change colors: update the CSS variables (`--ag-color-a`, `--ag-color-b`, `--ag-color-c`).
- Change animation speed: adjust `--ag-speed` (e.g., `2s`, `4s`).
- Change size: adjust `--ag-padding` and `font-size`.
- Change shape: adjust `--ag-radius`.

Accessibility tips
- Use semantic elements or add `aria-label` for icon-only buttons:
  `<button class="ag-button" aria-label="Subscribe">Subscribe</button>`
- Ensure sufficient color contrast for text over the gradient; consider a semi-opaque overlay or stronger text-shadow for readability.
- Keep keyboard focus visible (the repo includes a focus style).

File structure
- `index.html` — demo page
- `styles.css` — main CSS containing the animated gradient styles
- `Screenshot 2024-05-30 214310.png` — screenshot used in README

Contributing
- Found a bug or improvement? Open an issue.
- PRs welcome — fork, add a short description and demos when appropriate.
- Keep changes small and focused.

License
- MIT License — see LICENSE file.

Attribution
- Created by BinaryVortex
- If you use this button in a public project, a star on the repo is appreciated!

Contact
- GitHub: https://github.com/BinaryVortex
