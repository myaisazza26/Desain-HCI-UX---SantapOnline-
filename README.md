# Santap Online – Aplikasi Pemesanan Makanan

Aplikasi web pemesanan makanan online untuk tugas **Desain App Multi-platform & HCI/UX** (Sub-CPMK09-3-2 & Sub-CPMK09-3-4).
HTML, CSS, dan JavaScript murni (tanpa framework) yang dipisah per file, berjalan di HP, tablet, dan desktop, serta siap di-host di **GitHub Pages**.

## Struktur File
```
food-online/
├── index.html      # Kerangka halaman
├── css/
│   └── style.css   # Tampilan, tema, responsif
├── js/
│   ├── data.js     # Daftar menu & konstanta ongkir
│   ├── app.js      # Keranjang, checkout, validasi, status pesanan
│   └── theme.js    # Mode terang/gelap
└── README.md       # Dokumentasi
```

## Fitur
- Daftar 12 menu, filter kategori, dan pencarian
- Keranjang dengan tombol tambah/kurang, subtotal, ongkir (gratis di atas Rp100.000)
- Formulir pengiriman dengan validasi dan 3 metode pembayaran
- Pelacakan status pesanan (simulasi)
- Mode terang/gelap, keranjang tersimpan otomatis (localStorage)

## Cara Upload ke GitHub dan Aktifkan GitHub Pages
1. Buat akun di https://github.com lalu klik **New repository**.
2. Isi nama repositori, misalnya `food-online`, pilih **Public**, klik **Create repository**.
3. Klik **uploading an existing file**, tarik seluruh isi folder (`index.html`, folder `css`, folder `js`, dan `README.md`), lalu klik **Commit changes**.
4. Buka **Settings → Pages**.
5. Pada **Build and deployment**, pilih Source **Deploy from a branch**, Branch **main**, folder **/ (root)**, lalu **Save**.
6. Tunggu 1–2 menit. Alamat aplikasi: `https://USERNAME.github.io/food-online/`
7. Salin alamat itu ke laporan tugas.

Lewat terminal (opsional):
```bash
git init
git add .
git commit -m "Aplikasi Santap Online"
git branch -M main
git remote add origin https://github.com/USERNAME/food-online.git
git push -u origin main
```

## Pemetaan Prinsip HCI/UX
| Prinsip | Penerapan di aplikasi |
|---|---|
| Berpusat pada pengguna | Alur pendek: pilih menu → keranjang → data pengiriman → selesai |
| Umpan balik sistem | Notifikasi saat menambah/menghapus, badge total di bar bawah, status pesanan |
| Pencegahan & pemulihan kesalahan | Tombol **Batalkan** saat item dihapus atau keranjang dikosongkan, validasi formulir dengan pesan jelas |
| Konsistensi | Satu gaya tombol, istilah tetap ("Tambah", "Pesan sekarang") |
| Mengenali, bukan mengingat | Ikon makanan, kategori terlihat, ringkasan harga selalu tampil |
| Aksesibilitas | Kontras tinggi, label pada semua input, navigasi keyboard, fokus terlihat, target sentuh minimal 44px, tautan lewati konten, `prefers-reduced-motion` |
| Multi-platform / responsif | Grid fleksibel, bottom sheet di HP, dialog di desktop, area aman iOS, tema mengikuti sistem |
| Kebebasan pengguna | Mode terang/gelap, tutup dialog dengan Esc atau klik di luar |

## Pengembangan Lanjutan (Cloud App)
Untuk versi cloud nyata, ganti data `MENU` dan simulasi pesanan dengan API (misalnya Firebase atau Supabase) agar pesanan tersimpan di server dan status diperbarui real-time.
