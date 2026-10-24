# Mobile Schedule Alert V2

## Google Sheets + Apps Script
1. Create a Google Sheet, e.g. Mobile Schedule Alert DB.
2. Open Extensions > Apps Script.
3. Replace the default code with `Code.gs` from this bundle and Save.
4. Select `setup` in the function dropdown and Run once; authorize permissions.
5. Deploy > New deployment > Web app. Execute as: Me. Who has access: Anyone. Deploy and copy URL ending `/exec`.
6. In GitHub repository, replace `index.html` with this bundle's `index.html`, then Commit changes. Upload `manifest.json`, `sw.js`, and `icon.svg` too if they differ. `Code.gs` goes in Apps Script only.
7. Open the PWA > Tetapan. Paste Web App URL, click Simpan URL, then Sync sekarang.

Security: this prototype uses a public JSONP endpoint. Anyone who obtains the URL may be able to read or write schedule records. Do not store confidential data. For production, add authentication/authorization. Sync is manual and deletion/conflict handling is not production-ready. Export JSON before first sync. Reminders run only while app is open.
