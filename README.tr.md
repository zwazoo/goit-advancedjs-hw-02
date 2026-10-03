# Vanilla JS App

Vite tabanlı, iki sayfalı bir vanilla JavaScript projesi:

- **Timer** — flatpickr ile gelecekteki bir tarih ve saat seçin, ardından kalan
  gün, saat, dakika ve saniyeleri gösteren bir geri sayım başlatın. Start
  düğmesini etkinleştirmeden önce seçilen tarihin gelecekte olduğunu doğrular.
- **Snackbar** — yapılandırılabilir gecikme ve durum (fulfilled/rejected) ile
  bir Promise oluşturan form. Promise çözümlendiğinde veya reddedildiğinde
  iziToast bildirimi gösterir.

## Başlarken

1. [Node.js LTS](https://nodejs.org/en/) yüklü değilse yükleyin.
2. Bağımlılıkları yükleyin:
   ```bash
   npm install
   ```
3. Geliştirme sunucusunu başlatın:
   ```bash
   npm run dev
   ```
4. Tarayıcıda [http://localhost:5173](http://localhost:5173) adresini açın.

## Proje yapısı

```
src/
  1-timer.html        # Geri sayım timer sayfası
  2-snackbar.html     # Promise snackbar sayfası
  js/
    1-timer.js        # flatpickr başlatma, geri sayım mantığı
    2-snackbar.js     # Promise oluşturma + iziToast bildirimleri
  css/
    1-timer.css       # Timer sayfası stilleri
    2-snackbar.css    # Snackbar formu stilleri
  partials/           # Ortak HTML parçaları (header, footer)
  img/                # Görseller
```

## Dağıtım

Üretim sürümü, GitHub Actions aracılığıyla her `main` push'unda otomatik olarak
oluşturulur ve GitHub Pages'e dağıtılır. `package.json` dosyasındaki `--base`
bayrağı depo adına ayarlanmıştır:

```json
"build": "vite build --base=/goit-advancedjs-hw-02/"
```

## Kullanılan teknolojiler

- [Vite](https://vitejs.dev/)
- [flatpickr](https://flatpickr.js.org/) — tarih/saat seçici
- [iziToast](https://izitoast.marcelodolza.com/) — toast bildirimleri
- [vite-plugin-html-inject](https://github.com/donnikitos/vite-plugin-html-inject)
  — HTML parçaları için
