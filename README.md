# perpustakaanpendidikan
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
