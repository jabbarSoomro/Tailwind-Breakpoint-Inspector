# Tailwind Breakpoint Inspector

A lightweight browser-based inspector for Tailwind responsive classes. Paste HTML, JSX, TSX, or Vue template code and get a breakpoint coverage report, heatmap, gap detection, and auto-fix suggestions.

## Features

- Analyze Tailwind class usage across responsive breakpoints: `sm`, `md`, `lg`, `xl`, and `2xl`
- Visual element heatmap showing breakpoint coverage and base classes
- Metrics panel with average coverage, responsive ratio, and risk warnings
- Breakpoint usage and class group distribution charts
- Partial gap detection for elements missing some breakpoints
- Auto-fix suggestions for low coverage elements
- Export analysis as JSON
- Copy summary report to clipboard
- Drag & drop support for `.html`, `.htm`, `.jsx`, `.tsx`, `.vue`, and `.svelte` files
- Light/dark theme toggle

## Usage

1. Open `index.html` in a browser.
2. Paste your HTML, JSX, TSX, or Vue template into the input textarea.
3. Click **Analyze** or press `Ctrl+Enter`.
4. Review the generated:
   - metrics
   - breakpoint usage bars
   - coverage heatmap
   - responsive gap list
   - auto-fix suggestions
5. Use the export button to download a JSON report, or copy a summary report to the clipboard.

## Supported input

- Raw HTML with `class="..."`
- JSX/TSX with class attributes
- Vue templates with class attributes
- Drag and drop files supported: `.html`, `.htm`, `.jsx`, `.tsx`, `.vue`, `.svelte`

## How it works

- Extracts elements with a `class` attribute
- Detects breakpoint-prefixed Tailwind classes like `sm:`, `md:`, `lg:`, `xl:`, and `2xl:`
- Computes coverage score based on base classes plus responsive breakpoint coverage
- Flags elements with missing breakpoint support or no responsive classes
- Generates recommendations for missing breakpoint variants based on existing class patterns

## Notes

- The inspector is intended for quick static scanning of markup and class names.
- It does not execute Tailwind or resolve dynamic class names.
- Use it for draft reviews, responsive audits, and improving Tailwind breakpoint consistency.

## License

MIT

