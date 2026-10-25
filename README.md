# Sistem Akuntansi Persediaan Toko Mainan

Aplikasi web untuk membantu pencatatan persediaan dan transaksi toko mainan. Antarmuka menggunakan HTML, CSS, dan JavaScript, sedangkan data aplikasi disimpan menggunakan Supabase (PostgreSQL).

## Fitur

- **Dashboard**: ringkasan data dan informasi stok.
- **Data master**: pengelolaan barang, pemasok, dan pelanggan.
- **Transaksi**: pembelian, penjualan, penyesuaian stok, retur pembelian, dan retur penjualan.
- **Akuntansi**: jurnal umum dan buku besar.
- **Laporan**: laporan stok, pembelian, penjualan, kartu persediaan, laba rugi, dan neraca.
- **Pengaturan tampilan**: pilihan tema aplikasi.
- Pencarian data barang, pemasok, dan pelanggan pada formulir transaksi.

## Teknologi

- HTML5 dan CSS3
- JavaScript (tanpa framework)
- [Supabase](https://supabase.com/) untuk basis data PostgreSQL
- Supabase JavaScript Client v2, dimuat melalui jsDelivr CDN

## Struktur proyek

```text
UTS/
├── backend/
│   └── database.sql       # Skema dan data awal Supabase/PostgreSQL
├── frontend/
│   ├── css/
│   │   └── style.css      # Gaya dan tema antarmuka
│   ├── html/
│   │   └── index.html     # Halaman utama aplikasi
│   ├── img/
│   │   └── logo-ctoy.png  # Logo aplikasi
│   └── js/
│       ├── app.js         # Navigasi, tampilan, dan logika aplikasi
│       └── config.js      # Konfigurasi Supabase dan fungsi format
└── README.md
```

## Persiapan Supabase

1. Buat proyek di [Supabase](https://supabase.com/).
2. Buka **SQL Editor** pada proyek tersebut.
3. Jalankan isi file [`backend/database.sql`](backend/database.sql). Skrip membuat tabel barang, pemasok, pelanggan, pembelian beserta detailnya, penjualan beserta detailnya, akun, dan jurnal umum. Skrip juga menambahkan beberapa data contoh.
4. Di **Project Settings → API**, salin Project URL dan publishable/anon key.
5. Buka [`frontend/js/config.js`](frontend/js/config.js), lalu isi `SUPABASE_URL` dan `SUPABASE_ANON_KEY` dengan nilai proyek Supabase Anda.
6. Pastikan kebijakan akses (RLS) dan izin tabel Supabase telah sesuai dengan operasi yang digunakan aplikasi.

> Gunakan hanya publishable/anon key di aplikasi browser. Jangan pernah menaruh `service_role` key di kode frontend atau mengunggahnya ke GitHub.

## Menjalankan aplikasi

1. Pastikan konfigurasi Supabase dan skema basis data sudah disiapkan.
2. Buka folder proyek di Visual Studio Code.
3. Jalankan file `frontend/html/index.html` menggunakan server lokal, misalnya ekstensi **Live Server**.
4. Buka alamat lokal yang ditampilkan server pada browser.

Aplikasi memuat Supabase JavaScript Client dari CDN, sehingga koneksi internet diperlukan. Jika aplikasi tidak dapat membaca atau menyimpan data, periksa konfigurasi URL/key, tabel yang sudah dibuat, dan kebijakan akses Supabase.

## Catatan

File SQL menyediakan skema dasar persediaan, pembelian, penjualan, serta akuntansi. Pastikan skema dan kebijakan di proyek Supabase Anda cocok dengan modul yang akan digunakan. Aplikasi ini merupakan proyek berbasis web sisi-klien dan tidak menyediakan server aplikasi terpisah.
