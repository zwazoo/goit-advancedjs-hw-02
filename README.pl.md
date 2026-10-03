# Vanilla JS App

Projekt oparty na Vite z dwoma stronami:

- **Timer** — wybierz datę i godzinę w przyszłości za pomocą flatpickr, a
  następnie uruchom odliczanie wyświetlające dni, godziny, minuty i sekundy.
  Waliduje, czy wybrana data jest w przyszłości, przed odblokowaniem przycisku
  Start.
- **Snackbar** — formularz tworzący obietnicę (Promise) z konfigurowalnym
  opóźnieniem i stanem (fulfilled/rejected). Wyświetla powiadomienie iziToast po
  rozwiązaniu lub odrzuceniu obietnicy.

## Pierwsze kroki

1. Zainstaluj [Node.js LTS](https://nodejs.org/en/), jeśli nie masz go jeszcze
   zainstalowanego.
2. Zainstaluj zależności:
   ```bash
   npm install
   ```
3. Uruchom serwer deweloperski:
   ```bash
   npm run dev
   ```
4. Otwórz [http://localhost:5173](http://localhost:5173) w przeglądarce.

## Struktura projektu

```
src/
  1-timer.html        # Strona timera odliczającego
  2-snackbar.html     # Strona snackbara z obietnicą
  js/
    1-timer.js        # Inicjalizacja flatpickr, logika odliczania
    2-snackbar.js     # Tworzenie obietnicy + powiadomienia iziToast
  css/
    1-timer.css       # Style strony timera
    2-snackbar.css    # Style formularza snackbara
  partials/           # Wspólne fragmenty HTML (header, footer)
  img/                # Obrazy
```

## Wdrożenie

Wersja produkcyjna jest automatycznie budowana i wdrażana na GitHub Pages przy
każdym push do `main`. Flaga `--base` w `package.json` jest ustawiona na nazwę
repozytorium:

```json
"build": "vite build --base=/goit-advancedjs-hw-02/"
```

## Stos technologiczny

- [Vite](https://vitejs.dev/)
- [flatpickr](https://flatpickr.js.org/) — wybór daty i godziny
- [iziToast](https://izitoast.marcelodolza.com/) — powiadomienia toast
- [vite-plugin-html-inject](https://github.com/donnikitos/vite-plugin-html-inject)
  — fragmenty HTML
