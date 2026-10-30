MOBILE SCHEDULE PWA

Kandungan:
- index.html: PWA shell yang memaparkan Google Apps Script Web App sedia ada.
- manifest.webmanifest: nama, ikon dan tetapan pemasangan.
- sw.js: cache shell PWA. Data aplikasi masih memerlukan internet.
- icon.svg: ikon Mobile Schedule.
- Code.gs: versi Code.gs dengan X-Frame-Options dibenarkan supaya Web App boleh dipaparkan dalam shell PWA.

LANGKAH A — KEMAS KINI GOOGLE APPS SCRIPT
1. Buka projek Apps Script yang digunakan oleh URL Mobile Schedule.
2. Gantikan Code.gs dengan Code.gs dalam pakej ini. Jangan ubah fail Index.html yang sedia ada.
3. Save.
4. Deploy > Manage deployments > Edit (ikon pensel) > Version: New version > Deploy.
5. Pastikan URL Web App kekal sama. Jika URL berubah, kemas kini src iframe dalam index.html.

LANGKAH B — HOST PWA DI GITHUB PAGES
1. Cipta repository baharu di GitHub, contohnya mobile-schedule-pwa.
2. Muat naik enam fail: index.html, manifest.webmanifest, sw.js, icon.svg, icon-192.png dan icon-512.png. Code.gs dan README.txt tidak perlu dimuat naik ke Pages.
3. Repository > Settings > Pages.
4. Source: Deploy from a branch. Branch: main; folder: /(root). Save.
5. Tunggu GitHub Pages menerbitkan laman HTTPS.
6. Buka URL Pages yang diberi GitHub.

LANGKAH C — PASANG PADA TELEFON
- Android Chrome: buka URL GitHub Pages > menu ⋮ > Install app / Add to Home screen.
- iPhone Safari: Share > Add to Home Screen.

NOTA PENTING
- PWA ini ialah shell yang memaparkan Web App GAS dalam iframe. Semua data dan operasi masih menggunakan GAS/Google Sheets.
- Internet diperlukan untuk fungsi jadual, kenderaan dan simpanan data. Cache luar talian hanya menyimpan shell PWA, bukan pangkalan data.
- XFrameOptionsMode.ALLOWALL membenarkan laman lain memaparkan Web App. Gunakan hanya pada PWA milik sendiri dan tetapkan akses Web App dengan sesuai. Jangan kongsi URL jika akses data tidak sepatutnya umum.
