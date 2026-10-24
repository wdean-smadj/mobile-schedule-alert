# Mobile Schedule Alert (MSA) — Versi 1

## Ciri-ciri
- Dashboard hari ini dan minggu ini
- Tambah, edit, padam dan tandakan aktiviti selesai
- Kategori peribadi/sekolah/mesyuarat/panggilan/tugasan
- Ulangan mingguan
- Peringatan 5, 10, 15, 30 atau 60 minit
- Data disimpan pada peranti melalui localStorage
- Eksport/import sandaran JSON
- PWA asas dengan cache luar talian

## Cara uji pada komputer
1. Ekstrak ZIP.
2. Jalankan pelayan web setempat dalam folder ini, contohnya `python -m http.server 8000`.
3. Buka `http://localhost:8000` dalam Chrome.
4. Tambah aktiviti dan benarkan notifikasi.

## Cara pasang pada telefon
1. Muat naik semua fail ke hos yang menggunakan HTTPS (contoh GitHub Pages atau hosting sendiri).
2. Buka URL itu pada Chrome Android.
3. Pilih menu Chrome > Add to Home screen / Install app.
4. Buka aplikasi, pergi ke Tetapan > Benarkan notifikasi.

## Had penting
- Data versi ini disimpan secara setempat pada satu peranti/pelayar. Tiada penyegerakan antara telefon dan komputer.
- Semakan peringatan dibuat ketika aplikasi sedang terbuka. PWA statik tidak boleh menjamin alarm ketika pelayar ditutup atau telefon mengehadkan proses latar belakang.
- Push notification sebenar memerlukan backend, push subscription dan VAPID keys; ia belum termasuk dalam versi ini.
- Untuk penggunaan sebenar, gunakan HTTPS. Jangan simpan data sulit dalam peranti yang dikongsi.
