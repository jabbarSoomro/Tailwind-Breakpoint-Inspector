# Tailwind Breakpoint Inspector v2.0

A premium, lightweight, browser-based inspector for Tailwind responsive classes, style configurations, and live viewport simulations. Paste HTML, JSX, TSX, or Vue templates directly to audit breakpoint coverages, pseudo-states, class conflicts, responsive accessibility issues, and view real-time multi-device previews.

Runs **completely client-side** in a single static HTML file with zero build step dependencies.

---

## ✨ Features

### 🔍 Core Analytics
- **Responsive Breakpoint Coverage**: Audits class distribution across Tailwind breakpoints.
- **Visual Heatmap Table**: Highlights class coverage depth per line with dynamic tooltips and detail expansions.
- **Pseudo-State Auditing**: Audits pseudo-class prefixes like `hover:`, `focus:`, `dark:`, `group-hover:`, and `peer-focus:`.
- **Gaps & Auto-Fix Engine**: Identifies missing breakpoint classes and generates drop-in class suggestion fixes.

### ⚡ Live Multi-Screen Simulator (New)
- **Simultaneous Viewport Render**: Spins up sandboxed, side-by-side previews for all active breakpoints (`sm`, `md`, `lg`, `xl`, `2xl`).
- **Dynamic Tailwind CDN Configuration**: Feeds your active custom breakpoints config directly into the Tailwind dynamic compiler inside each preview screen for pixel-perfect matching.
- **Live Scale Zoom**: Features a responsive slider (30% to 100%) that scales down previews using CSS transforms while adjusting margins to keep previews adjacent without overlapping.
- **Compare Version Toggle**: Instantly switch the preview panel between Version A (Original) and Version B (Modified) while analyzing in comparison mode.

### 🛠️ Advanced Audit Tools
- **Side-by-Side Comparison**: Input Version A and Version B side-by-side to track coverage changes (improvement/regression deltas).
- **Class Conflict Detection**: Instantly flags contradictory classes (e.g. `block hidden` or `flex-row flex-col`) applied at the same breakpoint level.
- **Responsive Accessibility (A11y) Audit**: Scans elements for small font sizing, low padding touch targets on mobile clickable layers, and truncation without title hover descriptors.
- **Custom Breakpoint Configurator**: Add, remove, rename, or tweak min-width configurations to match your project's custom `tailwind.config.js` settings.
- **High-Performance Highlight Editor**: Custom textareas featuring responsive element size syncs, tab indentation, and on-the-fly syntax coloring for Tailwind classes.

### 💾 Integrations & Sharing
- **Analysis History**: Saves up to 20 past runs to `localStorage` with a visual sparkline trend chart mapping coverage growth.
- **Compressed Hash Sharing**: Generate instant shareable links encoding your inputs and breakpoint settings in the URL hash.
- **Export Capabilities**: Download reports as standard `.json` configurations or `.csv` spreadsheets.
- **Print & PDF Layouts**: Dedicated print styles optimized for exporting clean audit reports.
- **Theme Toggle**: Full dark mode toggle synchronized with custom styling.

---

## 🚀 Getting Started

1. Open [index.html](file:///c:/laragon/www/Tailwind-Breakpoint-Inspector/index.html) directly in any modern web browser.
2. Paste your markup or drag & drop files (.html, .jsx, .tsx, .vue, .svelte) directly onto the editor panel.
3. Click **Analyze** or press `Ctrl + Enter`.
4. Review the generated reports, heatmap cards, accessibility items, and the Live Multi-Screen simulator.

---

## ⚙️ Technical Details

- **Parser Engine**: Extracts element tags and attribute arrays using a lightweight browser RegExp match parser.
- **Dynamic Config**: Adapts all audit rules and simulation layouts on the fly based on settings stored in local caches.
- **Chunked Rendering**: Employs asynchronous lazy rendering (chunking elements in batches of 150) to prevent thread freezes when analyzing massive templates containing thousands of tags.
- **Sandboxed Rendering**: Previews use the `srcdoc` iframe API to guarantee sandboxing and avoid Same-Origin console errors.

---

## 📄 License

MIT
