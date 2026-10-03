# Vanilla JS App

Proiect bazat pe Vite cu două pagini:

- **Timer** — alege o dată și oră viitoare cu flatpickr, apoi pornește un
  countdown care afișează zilele, orele, minutele și secundele rămase. Validează
  că data selectată este în viitor înainte de a activa butonul Start.
- **Snackbar** — un formular care creează o promisiune (Promise) cu o întârziere
  și o stare configurabilă (fulfilled/rejected). Afișează o notificare iziToast
  când promisiunea se rezolvă sau este respinsă.

## Pornire

1. Instalează [Node.js LTS](https://nodejs.org/en/) dacă nu este deja instalat.
2. Instalează dependențele:
   ```bash
   npm install
   ```
3. Pornește serverul de dezvoltare:
   ```bash
   npm run dev
   ```
4. Deschide [http://localhost:5173](http://localhost:5173) în browser.

## Structura proiectului

```
src/
  1-timer.html        # Pagina timerului countdown
  2-snackbar.html     # Pagina snackbar cu promisiune
  js/
    1-timer.js        # Inițializare flatpickr, logica countdown
    2-snackbar.js     # Creare promisiune + notificări iziToast
  css/
    1-timer.css       # Stiluri pagina timer
    2-snackbar.css    # Stiluri formular snackbar
  partials/           # Fragmente HTML comune (header, footer)
  img/                # Imagini
```

## Deployment

Versiunea de producție este construită și distribuită automat pe GitHub Pages la
fiecare push pe `main`. Flag-ul `--base` din `package.json` este setat la numele
repository-ului:

```json
"build": "vite build --base=/goit-advancedjs-hw-02/"
```

## Tehnologii utilizate

- [Vite](https://vitejs.dev/)
- [flatpickr](https://flatpickr.js.org/) — selector de dată și oră
- [iziToast](https://izitoast.marcelodolza.com/) — notificări toast
- [vite-plugin-html-inject](https://github.com/donnikitos/vite-plugin-html-inject)
  — fișiere HTML parțiale
