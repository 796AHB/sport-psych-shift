# Sport Psych Shift · PWA

Game psikologi sukan (Open Day, Tangga Kerjaya, Sukan Asia, Sukan Para Asia). Fail statik sahaja, tiada server khas diperlukan.

## Kandungan
- `index.html` – keseluruhan game (satu fail)
- `manifest.webmanifest` – maklumat aplikasi (nama, ikon, mendatar/landscape)
- `sw.js` – service worker supaya boleh dipasang dan main tanpa internet selepas buka kali pertama
- `icons/` – ikon aplikasi

## Cara deploy (pilih satu)
**Netlify Drop (paling mudah):** buka https://app.netlify.com/drop, seret folder `sport-psych-shift` ke dalam halaman. Siap, dapat link HTTPS.

**GitHub Pages:** buat repo baharu, muat naik semua fail dalam folder ini ke root repo, kemudian Settings → Pages → Deploy from branch → `main` / root.

**Vercel / Cloudflare Pages / server sendiri:** muat naik folder ini sebagai laman statik. Pastikan ia dihidangkan melalui **HTTPS** (wajib untuk PWA dan butang Install).

## Nota
- Kali pertama dibuka perlu internet (three.js dan fon dimuat dari CDN), selepas itu ia disimpan dalam cache.
- Bila kemas kini `index.html`, tukar nilai `CACHE` dalam `sw.js` (cth. `sport-psych-v22`) supaya pemain dapat versi baharu.
- Jangan buka `index.html` terus dari komputer (file://). Service worker hanya berfungsi melalui http(s). Untuk uji di komputer: `npx serve .` atau `python3 -m http.server`.
