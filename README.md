# Sistem Informasi Perpustakaan Pendidikan

Aplikasi web perpustakaan berbasis PHP native (tanpa framework) dengan tiga level akses pengguna: **Admin**, **Petugas**, dan **User (Siswa/Anggota)**.

## 📁 Struktur Folder

```
perpustakaan/
│
├── admin/                     # Halaman khusus Administrator
│   ├── anggota.php            # Kelola data anggota/siswa
│   ├── buku.php                # Kelola data buku
│   ├── index.php               # Dashboard admin (statistik & grafik)
│   └── transaksi.php           # Lihat & kelola data transaksi peminjaman
│
├── petugas/                   # Halaman khusus Petugas Perpustakaan
│   ├── anggota.php             # Kelola data anggota
│   ├── buku.php                 # Kelola data buku
│   ├── cetak_transaksi.php      # Cetak laporan transaksi
│   ├── edit_anggota.php         # Form edit data anggota
│   ├── edit_buku.php            # Form edit data buku
│   ├── edit_transaksi.php       # Form edit data transaksi
│   ├── hapus_anggota.php        # Proses hapus data anggota
│   ├── hapus_buku.php           # Proses hapus data buku
│   ├── index.php                 # Dashboard petugas
│   ├── kembali.php               # Proses pengembalian buku
│   ├── proses_selesai.php        # Proses penyelesaian transaksi
│   ├── tambah_anggota.php        # Form tambah anggota baru
│   ├── tambah_buku.php           # Form tambah buku baru
│   ├── tambah_transaksi.php      # Form tambah transaksi peminjaman
│   └── transaksi.php             # Daftar seluruh transaksi
│
├── user/                       # Halaman khusus User (Siswa/Anggota)
│   ├── batalkan_pinjam.php      # Proses pembatalan peminjaman
│   ├── buku.php                  # Daftar koleksi buku
│   ├── detail_buku.php           # Detail informasi buku
│   ├── edit_profil.php           # Form edit profil pengguna
│   ├── ganti_password.php        # Form ganti password
│   ├── index.php                  # Dashboard user (koleksi buku & rating)
│   ├── logout_user.php            # Proses logout user
│   ├── pinjam.php                 # Proses peminjaman buku
│   ├── profil.php                 # Halaman profil pengguna
│   └── riwayat.php                # Riwayat peminjaman user
│
├── gambar/                     # Folder penyimpanan cover/gambar buku
│   └── *.jpeg / *.jpg           # File gambar sampul buku
│
├── index.php                    # Landing page utama
├── koneksi.php                  # File koneksi ke database (MySQL)
├── login.php                    # Halaman login (multi-role: admin/petugas/user)
├── logout.php                   # Proses logout (admin/petugas)
├── register_admin.php           # Form pendaftaran akun admin/petugas
├── video.php                    # Halaman pemutar video panduan
└── video.mp4                    # File video panduan penggunaan
```

## 👥 Hak Akses Pengguna

| Role | Deskripsi | Folder |
|------|-----------|--------|
| **Admin** | Mengelola seluruh sistem: buku, anggota, transaksi, serta melihat statistik & grafik peminjaman | `/admin` |
| **Petugas** | Mengelola operasional harian: input/edit/hapus buku & anggota, proses transaksi peminjaman-pengembalian, cetak laporan | `/petugas` |
| **User (Siswa)** | Melihat koleksi buku, meminjam buku, memberi rating & ulasan, melihat riwayat peminjaman, mengelola profil | `/user` |

## 🗄️ Database

Koneksi database dikonfigurasi pada file `koneksi.php`. Tabel utama yang digunakan antara lain:
- `users` — akun admin & petugas
- `anggota` — akun/data siswa
- `buku` — data koleksi buku
- `transaksi` — data peminjaman & pengembalian buku
- `rating` — rating & ulasan buku dari user

## 🚀 Cara Menjalankan (Local - XAMPP)

1. Salin folder `perpustakaan` ke direktori `htdocs` pada instalasi XAMPP.
2. Jalankan **Apache** dan **MySQL** melalui XAMPP Control Panel.
3. Buat database dan sesuaikan kredensial koneksi pada `koneksi.php`.
4. Akses aplikasi melalui browser: `http://localhost/perpustakaan/`.
5. Login sesuai role (Admin / Petugas / Siswa) melalui halaman `login.php`.

## 🛠️ Teknologi yang Digunakan

- **Backend:** PHP (native, mysqli)
- **Database:** MySQL
- **Frontend:** Bootstrap 5, Bootstrap Icons, SweetAlert2
- **Grafik/Statistik:** Chart.js
