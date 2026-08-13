# 💰 Laporan BOS

Aplikasi desktop untuk manajemen keuangan dana BOS sekolah — dibangun dengan **Electron + Vite + Tailwind CSS**.

## Fitur

- **Dashboard** — ringkasan saldo, pemasukan/pengeluaran, progres RKAS
- **Buku Kas Umum (BKU)** — catat transaksi kas, saldo berjalan otomatis
- **RKAS** — rencana & realisasi anggaran per kegiatan
- **Pajak** — pencatatan pajak dipungut & status setor
- **Laporan** — cetak BKU bulanan dengan kop surat resmi & tanda tangan
- **Profil Sekolah** — data kop surat (nama sekolah, NPSN, kepala sekolah, bendahara)
- Data tersimpan lokal di perangkat (electron-store), tidak perlu internet

## Menjalankan (Development)

```bash
npm install
npm run electron:dev
```

Ini akan menjalankan Vite dev server + Electron secara bersamaan.

## Build Aplikasi Desktop

```bash
npm run dist:win     # Windows (.exe installer)
npm run dist:mac     # macOS (.dmg)
npm run dist:linux   # Linux (.AppImage)
```

Hasil build ada di folder `release/`.

## Struktur Folder

```
├── electron/          # Proses utama Electron (main.js, preload.js)
├── src/
│   ├── pages/          # Setiap halaman (dashboard, bku, rkas, pajak, laporan, profil)
│   ├── utils/           # Helper (db.js untuk penyimpanan, format.js untuk format Rupiah/tanggal)
│   ├── main.js          # Entry point + layout sidebar + router
│   └── style.css
├── public/               # Icon aplikasi
├── index.html
├── vite.config.js
├── tailwind.config.js
└── package.json
```

## Teknologi

- Electron 31
- Vite 5
- Tailwind CSS 3
- electron-store (penyimpanan data lokal)
- electron-builder (build installer)

## Lisensi

MIT
