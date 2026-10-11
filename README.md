# Sistem Akuntansi Persediaan Toko Mainan

Aplikasi web untuk membantu pengelolaan persediaan barang dan pencatatan transaksi toko mainan. Aplikasi menggunakan HTML, CSS, dan JavaScript pada sisi frontend, serta Supabase dengan PostgreSQL untuk penyimpanan data.

## Fitur

- **Dashboard persediaan** untuk melihat ringkasan data dan transaksi.
- **Data barang** untuk mengelola informasi barang dan stok.
- **Data pemasok dan pelanggan** untuk menyimpan data pihak terkait transaksi.
- **Pembelian dan penjualan** untuk mencatat transaksi barang.
- **Penyesuaian stok** untuk mencatat perubahan persediaan.
- **Jurnal umum dan buku besar** untuk melihat pencatatan akuntansi.

## Teknologi

- HTML, CSS, dan JavaScript
- Supabase
- PostgreSQL
- Supabase JavaScript Client v2 melalui CDN jsDelivr

## Struktur Proyek

```text
.
├── .gitignore
├── README.md
└── UTS/
    ├── backend/
    │   └── database.sql
    └── frontend/
        ├── css/
        │   └── style.css
        ├── html/
        │   └── index.html
        └── js/
            ├── app.js
            └── config.js
```

## Persyaratan

- Visual Studio Code
- Browser, seperti Google Chrome atau Microsoft Edge
- Koneksi internet
- Project Supabase yang aktif
- Ekstensi Live Server di Visual Studio Code

## Cara Menjalankan

1. Buka folder utama proyek di Visual Studio Code. Folder ini berisi `README.md` dan folder `UTS`.
2. Buat project di [Supabase](https://supabase.com/) jika belum memilikinya.
3. Buka **SQL Editor** di dashboard Supabase, lalu jalankan isi file `UTS/backend/database.sql`.
4. Buka `UTS/frontend/js/config.js`. Isi `SUPABASE_URL` dan `SUPABASE_ANON_KEY` dengan Project URL dan publishable key (atau anon key) dari pengaturan API Supabase.
5. Buka `UTS/frontend/html/index.html`, lalu pilih **Open with Live Server**.
6. Periksa halaman aplikasi di browser. Pastikan koneksi internet tersedia agar aplikasi dapat memuat Supabase Client dan terhubung ke project Supabase.

Jalankan aplikasi melalui server lokal seperti Live Server. Jangan membuka halaman dengan alamat `file://`.

## Batasan

Versi saat ini belum menyediakan modul retur pembelian atau retur penjualan. Aplikasi juga belum menyediakan autentikasi pengguna dan pengaturan hak akses berbasis pengguna.

## Pemecahan Masalah

- **`Failed to fetch` atau `DNS_PROBE_FINISHED_NXDOMAIN`:** periksa koneksi internet, Project URL di `config.js`, status project Supabase, dan akses jaringan ke Supabase.
- **Tabel tidak ditemukan:** pastikan seluruh script `UTS/backend/database.sql` berhasil dijalankan pada project Supabase yang benar.
- **Akses ditolak atau data tidak muncul:** periksa kebijakan akses/RLS tabel di Supabase serta key yang digunakan pada `config.js`.
