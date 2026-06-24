# Tailwind Breakpoint Inspector v2.0

A premium, lightweight, browser-based inspector for Tailwind responsive classes and style configurations. Paste HTML, JSX, TSX, or Vue templates directly to audit breakpoint coverages, interactive states, class conflicts, responsive accessibility issues, and auto-fix recommendations.

Runs **completely client-side** in a single static HTML file with zero build step dependencies.

---

## ✨ Features

### 🔍 Core Analytics
- **Responsive Breakpoint Coverage**: Audits class distribution across Tailwind breakpoints.
- **Visual Heatmap Table**: Highlights class coverage depth per line with dynamic tooltips and detail expansions.
- **Interactive State Auditing**: Audits pseudo-class prefixes like `hover:`, `focus:`, `dark:`, `group-hover:`, and `peer-focus:`.
- **Gaps & Auto-Fix Engine**: Identifies missing breakpoint classes and generates drop-in class suggestion fixes.

### ⚡ Advanced Tools (New in v2.0)
- **Side-by-Side Comparison**: Input Version A and Version B side-by-side to track coverage changes (improvement/regression deltas).
- **Class Conflict Detection**: Instantly flags contradictory classes (e.g. `block hidden` or `flex-row flex-col`) applied at the same breakpoint level.
- **Responsive Accessibility (A11y) Audit**: Scans elements for small font sizing, low padding touch targets on mobile clickable layers, and truncation without title hover descriptors.
- **Custom Breakpoint Configurator**: Add, remove, rename, or tweak min-width configurations to match your project's custom `tailwind.config.js` settings.
- **High-Performance Highlight Editor**: Custom textareas featuring responsive element size syncs, tab indentation, and on-the-fly syntax coloring for Tailwind classes.

### 💾 Integrations & Sharing
- **Analysis History**: Saves up to 20 past runs to `localStorage` with a visual sparkline trend chart mapping coverage growth.
- **Compressed Hash Sharing**: Generate instant shareable links encoding your inputs and breakpoint settings in the URL hash.
- **Export Capabilities**: Download reports as standard `.json` configurations or `.csv` spreadsheet sheets.
- **Print & PDF Layouts**: Dedicated print styles optimized for exporting clean audit papers.
- **Theme Toggle**: Full dark mode toggle synchronized with custom styling.

---

## 🚀 Getting Started

1. Open [index.html](file:///c:/laragon/www/Tailwind-Breakpoint-Inspector/index.html) directly in any web browser.
2. Paste your markup or drag & drop files (.html, .jsx, .tsx, .vue, .svelte) directly onto the editor panel.
3. Click **Analyze** or press `Ctrl + Enter`.
4. Review the generated reports, heatmap cards, accessibility items, and conflicts listing.

---

## 🛠️ How it Works

- **Parser Engine**: Extracts element tags and attribute arrays using a lightweight browser RegExp match parser.
- **Dynamic Config**: Adapts all audit rules on the fly based on settings stored in local caches.
- **Chunked Rendering**: Employs asynchronous lazy rendering (chunking elements in batches of 150) to prevent thread freezes when analyzing massive templates containing thousands of tags.

---

## 📄 License

MIT
