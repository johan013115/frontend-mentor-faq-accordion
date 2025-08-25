# FAQ Accordion — Responsive Frontend Mentor Project in JS 🚀

[![Releases](https://img.shields.io/badge/Releases-View-blue?logo=github)](https://github.com/johan013115/frontend-mentor-faq-accordion/releases)

An interactive, responsive FAQ accordion built with HTML, CSS, and JavaScript. This repo follows a Frontend Mentor challenge and focuses on pixel-accurate layout, accessible interactions, and a dark/light theme toggle.

Live releases and downloadable builds are available on the Releases page. Download and execute the release file from https://github.com/johan013115/frontend-mentor-faq-accordion/releases to run a packaged build (open the included index.html in your browser).

---

![Hero preview of FAQ accordion UI](https://images.unsplash.com/photo-1515879218367-8466d910aaa4?auto=format&fit=crop&w=1400&q=80)

Badges
- Topics: 5th-month · accordion · css · frontend-mentor · git · github · html · javascript · lighthouse · netlify · perfectpixel · project · theme-toggle · vscode
- Build: local static site
- Accessibility: keyboard-friendly, ARIA attributes

Quick links
- Releases (download and execute): https://github.com/johan013115/frontend-mentor-faq-accordion/releases
- Repository: frontend-mentor-faq-accordion

Why this project? 🎯
- Practice DOM patterns: show/hide, sibling control, and smooth transitions.
- Improve CSS skills: fluid layout, Flexbox, CSS variables, and responsive breakpoints.
- Improve accessibility: proper ARIA roles, keyboard support, and focus management.
- Improve performance: small bundle, no frameworks, Lighthouse-friendly.

Features ✅
- Fully responsive layout that matches the Frontend Mentor design.
- Accessible accordion:
  - Proper ARIA roles (button, region).
  - Keyboard controls: Tab, Enter, Space to toggle; Up/Down to navigate items.
  - Focus indicators and skip link support.
- Smooth height transitions with CSS and JS for cross-browser consistency.
- Theme toggle (light / dark) using CSS variables and localStorage persistence.
- Minimal JavaScript, no external frameworks.
- High Lighthouse scores for performance and accessibility when hosted statically.
- Deploy-ready: drop into Netlify, Vercel, GitHub Pages, or any static host.

Demo and Screenshots
- Desktop preview: shows 2-column layout with questions and answers.
- Mobile preview: single-column stacked accordion with touch-friendly targets.

Screenshots
![Desktop accordion example](https://raw.githubusercontent.com/johan013115/frontend-mentor-faq-accordion/main/assets/desktop-preview.png)
![Mobile accordion example](https://raw.githubusercontent.com/johan013115/frontend-mentor-faq-accordion/main/assets/mobile-preview.png)

If these images fail to load, check the Releases page and the repository assets.

Getting started — local (no build step)
1. Clone the repo
```bash
git clone https://github.com/johan013115/frontend-mentor-faq-accordion.git
cd frontend-mentor-faq-accordion
```
2. Open index.html in your browser or run a local server
```bash
# using Python 3
python -m http.server 8000
# then visit http://localhost:8000
```

Installable release
- Visit the Releases page and download the latest zip or tarball.
- Extract the archive.
- Execute the included index.html file in a modern browser.
- The Releases page contains packaged builds that match the live preview.

If the Releases link does not work, check the Releases section in this repository. The direct link is https://github.com/johan013115/frontend-mentor-faq-accordion/releases

Folder structure
- /index.html — single-page demo and markup
- /styles/ — CSS sources and compiled files
  - base.css — reset and base typographic rules
  - components/accordion.css — accordion layout and transitions
  - theme.css — CSS variables and theme toggle
- /scripts/ — JavaScript sources
  - accordion.js — main accordion behavior and keyboard handlers
  - theme.js — theme toggle and persistence
- /assets/ — images and design previews
- /LICENSE

Core implementation notes
- HTML
  - Use <button> for each question. Wrap answer content in a region with aria-hidden when collapsed.
  - Use data attributes to link buttons to panels for cleaner JS.
- CSS
  - Use CSS variables for colors, spacing, and breakpoints.
  - Use max-height transitions with a computed value in JS to allow smooth open/close.
  - Use prefers-reduced-motion to disable animation for users who set that preference.
- JavaScript
  - Minimal DOM operations: query selectors, class toggles, and inline style changes.
  - Use event delegation where sensible.
  - Keyboard handling:
    - Enter / Space: toggle focused item.
    - Arrow Up / Arrow Down: move focus to previous / next button.
    - Home / End: focus first / last button.
  - Theme toggle persists to localStorage. On load, script reads saved theme and applies it.

Accessibility checklist
- Each accordion button uses aria-expanded set to true/false.
- Each panel uses role="region" and aria-labelledby pointing to the button id.
- Keyboard navigation follows WAI-ARIA Authoring Practices for accordion widgets.
- Visible focus styles for keyboard users.
- Color contrast meets WCAG AA for text.

Performance and Lighthouse tips
- Keep CSS and JS files small. This project bundles minimal code.
- Use proper caching headers on your host.
- Use critical CSS for above-the-fold content when you scale the project.
- Use SVG icons inline or as a sprite for smaller payload.
- Test with Lighthouse and address any accessibility or best-practice flags.

Theme toggle
- The project uses CSS variables for color and a simple toggle button.
- Theme selection persists in localStorage under key "fm-faq-theme".
- The theme script toggles a data-theme attribute on <html> and updates the toggle button label.

Testing checklist
- Manual:
  - Run on desktop and mobile widths.
  - Test with keyboard only navigation.
  - Disable JS to see accessible baseline content.
- Automated:
  - Run Lighthouse for performance and accessibility.
  - Use axe-core for automated accessibility checks.
  - Run Lighthouse in CI for regression detection.

Deployment
- Host as a static site.
- Recommended hosts:
  - Netlify: drag and drop the publish folder or connect the repo.
  - GitHub Pages: use the docs or main branch.
  - Vercel: connect the repo and deploy.

Tips for pixel-perfect match
- Use the original design's base font and spacing tokens.
- Use precise line-height and letter-spacing for headings.
- Use the provided mockup image as a background reference and compare with overlay tools.

Contribution guide
- Fork the repo.
- Create a feature branch: git checkout -b feat/your-idea
- Keep changes focused and commit early.
- Open a pull request with a clear description and screenshots if applicable.
- Follow the existing file structure and naming conventions.
- Label changes: fix, feat, perf, doc.

Release management
- Tag releases with semantic versioning.
- Include changelog entries for each release.
- Attach packaged zip or tar.gz with index.html and assets so users can download and run the demo.
- Users can download and execute the packaged index.html file from the Releases page.

License
- The project uses the MIT License. See LICENSE file for full text.

Credits and resources
- Frontend Mentor challenge: base design and layout brief.
- Pattern references:
  - WAI-ARIA Authoring Practices — accordion pattern.
  - CSS Tricks — accessible accordion tips.
- Image credits: Unsplash and repository assets.

Contact
- Open an issue for bugs or feature requests.
- Submit pull requests for improvements or fixes.

Releases
[![Download Release](https://img.shields.io/badge/Download%20Release-zip-blue?logo=github)](https://github.com/johan013115/frontend-mentor-faq-accordion/releases)

Download and execute the release file from https://github.com/johan013115/frontend-mentor-faq-accordion/releases to run a packaged build (open the included index.html in your browser).

Changelog highlights (sample)
- v1.2.0 — Added keyboard Home/End navigation and improved transitions.
- v1.1.0 — Theme toggle with localStorage; improved contrast.
- v1.0.0 — Initial challenge release with responsive layout and accessible accordion.

Files to look at first
- index.html — start here to see the markup.
- scripts/accordion.js — core behavior for toggle and keyboard.
- styles/components/accordion.css — transitions and responsive rules.

Common issues
- If panels jump during open/close, ensure JS sets max-height computed from scrollHeight.
- If keyboard arrows skip items, ensure all question buttons are focusable and in DOM order.
- If theme does not persist, check localStorage permissions in the browser.

Fork, build, and ship your version.