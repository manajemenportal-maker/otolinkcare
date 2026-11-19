# OtoLink Care PWA

## Isi paket
- `index.html` — aplikasi pelayanan pelanggan
- `manifest.webmanifest` — konfigurasi instalasi PWA
- `sw.js` — service worker/offline cache
- `icon-192.png`, `icon-512.png` — ikon aplikasi

## Cara menjalankan
1. Upload seluruh isi folder ini ke hosting dengan HTTPS, misalnya pada folder `/keluhan/` di domain OtoLink.
2. Pastikan alamat menjadi `https://otolink.id/keluhan/` (atau sesuaikan URL yang dipilih).
3. Buka melalui Chrome, lalu pilih Install app / Add to Home Screen.

## Konfigurasi kontak
Buka `index.html`, cari `const CONFIG={whatsapp:"",email:""};` lalu isi:
- whatsapp: nomor internasional tanpa tanda +, contoh `62812xxxxxxx`
- email: email pelayanan resmi

## Catatan penting sebelum go-live
Versi ini adalah frontend PWA yang menyimpan tiket pada browser/perangkat pengguna (`localStorage`). Karena belum terhubung ke backend, laporan tidak otomatis masuk ke admin pusat dan tidak dapat dilihat lintas perangkat. Lampiran hanya dibatasi dan nama file tidak diunggah. Untuk operasional nyata, sambungkan formulir, lampiran, status tiket, dan dashboard admin ke Firebase/Firestore atau backend server. Hosting harus menggunakan HTTPS agar PWA dan service worker aktif.
