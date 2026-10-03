# Vanilla JS App

A Vite-based vanilla JavaScript project with two pages:

- **Timer** — pick a future date/time with a flatpickr datepicker, then start a
  countdown that shows days, hours, minutes, and seconds remaining. Validates
  that the selected date is in the future before enabling the Start button.
- **Snackbar** — a form that creates a promise with a configurable delay and
  fulfilled/rejected state. Shows an iziToast notification when the promise
  resolves or rejects.

## Getting started

1. Install [Node.js LTS](https://nodejs.org/en/) if not already installed.
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the dev server:
   ```bash
   npm run dev
   ```
4. Open [http://localhost:5173](http://localhost:5173) in your browser.

## Project structure

```
src/
  1-timer.html        # Countdown timer page
  2-snackbar.html     # Promise snackbar page
  js/
    1-timer.js        # Flatpickr init, countdown logic
    2-snackbar.js     # Promise creation + iziToast notifications
  css/
    1-timer.css       # Timer page styles
    2-snackbar.css    # Snackbar form styles
  partials/           # Shared HTML fragments (header, footer)
  img/                # Images
```

## Deploy

Production build is deployed to GitHub Pages via GitHub Actions on every push to
`main`. The `--base` flag in `package.json` is set to the repository name:

```json
"build": "vite build --base=/goit-advancedjs-hw-02/"
```

## Tech stack

- [Vite](https://vitejs.dev/)
- [flatpickr](https://flatpickr.js.org/) — date/time picker
- [iziToast](https://izitoast.marcelodolza.com/) — toast notifications
- [vite-plugin-html-inject](https://github.com/donnikitos/vite-plugin-html-inject)
  — HTML partials
