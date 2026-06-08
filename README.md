# intake

A sleek, single-file client intake form for freelance web projects. Drop the link, collect structured project details, get a clean submission straight to your inbox — no backend, no database, no build step.

Built under the **devforge** brand.

---

## Features

- **Single file, zero dependencies** — just `intake.html`. Host it anywhere static.
- **Three-state theming** — system / light / dark, cycled via the top-right toggle. Defaults to the visitor's OS preference and live-reacts to OS theme changes.
- **No FOUC** — theme resolves before first paint via an inline head script.
- **Live progress bar** — fills as required fields complete, reducing form fatigue.
- **Chip-style inputs** — tappable, mobile-friendly toggles instead of raw checkboxes/radios.
- **Async submit** — posts to Formspree, then swaps to an inline success state (no jarring redirect).
- **Sensible defaults** — common selections pre-checked so non-technical clients aren't staring at a blank wall.

---

## Setup

1. **Create a Formspree form** at [formspree.io](https://formspree.io) and grab your form ID.
2. **Swap the placeholder** in `intake.html`:
   ```html
   <form id="intakeForm" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
   Replace `YOUR_FORM_ID` with your real endpoint (e.g. `f/abcdwxyz`).
3. **Deploy** — drag `intake.html` onto [Netlify Drop](https://app.netlify.com/drop) or push to any static host.
4. **Confirm the endpoint** — submit the form once yourself and click the Formspree confirmation email. Until you do, live submissions won't reach your inbox.

---

## Stack

- Vanilla HTML / CSS / JS — no framework, no build
- CSS custom properties for theming (`data-theme` + `data-theme-mode`)
- [Formspree](https://formspree.io) for form handling
- Fonts: Fraunces (display) + Sora (body) via Google Fonts

---

## Customizing

- **Theme colors** live in the `:root` token blocks at the top of the `<style>` — edit the `--accent`, `--bg`, etc. for each theme.
- **Form fields** are plain HTML inside numbered `.section` blocks — add, remove, or reorder freely. The progress bar auto-counts anything marked `required`.

---

Built by [bkness](https://github.com/bkness) · devforge
