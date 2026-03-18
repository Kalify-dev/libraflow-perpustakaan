<div align="center">

<h1>📚 LibraFlow — Sistem Manajemen Perpustakaan Modern</h1>

<p><em>Solusi digital lengkap untuk perpustakaan sekolah, kampus, dan institusi — dibangun dengan Laravel 12</em></p>

![Laravel](https://img.shields.io/badge/Laravel-12.x-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-8.2+-777BB4?style=for-the-badge&logo=php&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-3.x-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
[![Live Demo](https://img.shields.io/badge/🚀_Live_Demo-Railway-blueviolet?style=for-the-badge)](https://web-production-d6a51.up.railway.app/)

<br/>

> **🎯 Dirancang untuk sekolah, kampus, dan perpustakaan umum yang ingin go digital dengan tampilan modern dan fitur lengkap.**

<br/>

### 🌐 [👉 Coba Demo Live Sekarang](https://web-production-d6a51.up.railway.app/)

| Role | Email | Password |
|------|-------|----------|
| 🧑‍💼 **Guest / Demo** | demo@perpus.com | percobaan123 |

</div>

---

## 🖼️ Screenshot

### 🌐 Landing Page
![Landing Page](screenshots/01-landing-page.png)

### 🔐 Halaman Login
![Login Page](screenshots/02-login-page.png)

### 📊 Dashboard Admin
![Dashboard](screenshots/03-dashboard.png)

### 📚 Katalog Koleksi Buku
![Katalog Buku](screenshots/04-katalog-buku.png)

### 👥 Manajemen Anggota
![Manajemen Anggota](screenshots/05-manajemen-anggota.png)

---

## ✨ Fitur Unggulan

### 📖 Manajemen Koleksi Buku
- ✅ CRUD buku dengan **cover, barcode, dan QR code** otomatis
- ✅ Manajemen **eksemplar buku** (book copies) per item
- ✅ Kategorisasi buku, penulis, dan penerbit
- ✅ **Import buku massal** via file Excel
- ✅ Tandai buku sebagai **featured / unggulan**
- ✅ Dukungan **buku digital (PDF)** yang bisa dibaca langsung di browser
- ✅ **Audit stok** buku secara berkala

### 👥 Manajemen Anggota
- ✅ Pendaftaran anggota dengan **foto profil** dan data institusi (sekolah/kelas/NIS)
- ✅ **Sistem poin & badge** (gamifikasi) untuk mendorong minat baca
- ✅ Riwayat peminjaman per anggota
- ✅ Export data anggota ke Excel/PDF

### 📋 Peminjaman & Pengembalian
- ✅ Alur peminjaman yang mudah dan cepat
- ✅ **Sistem reservasi** buku (anggota bisa pesan buku sebelum tersedia)
- ✅ **Notifikasi otomatis** untuk buku yang siap diambil / hampir jatuh tempo
- ✅ Tracking status: *Dipinjam → Dikembalikan → Terlambat*

### 💰 Sistem Denda
- ✅ Kalkulasi denda otomatis berdasarkan keterlambatan
- ✅ **Pengaturan denda fleksibel** (tarif per hari, batas maksimum, dll.)
- ✅ Riwayat pembayaran denda

### 📊 Laporan & Analitik
- ✅ Dashboard dengan statistik real-time
- ✅ Laporan peminjaman, pengembalian, dan denda
- ✅ **Export laporan** ke PDF & Excel
- ✅ Grafik tren peminjaman

### ⚙️ Pengaturan Sistem
- ✅ **Pengaturan global**: nama perpustakaan, logo, kontak
- ✅ Manajemen staff dengan **role-based access** (Admin, Staff, Guest, Siswa)
- ✅ **Pengumuman** untuk anggota
- ✅ **Activity log** setiap aksi yang dilakukan pengguna
- ✅ **Sistem request buku** dari anggota ke pustakawan

### 🌐 Halaman Publik
- ✅ **Landing page** menarik dengan pencarian buku
- ✅ **Katalog online** yang bisa diakses tanpa login
- ✅ Kartu anggota digital dengan **QR Code**

### 🔒 Keamanan & Akses
- ✅ Sistem **RBAC** (Role Based Access Control) dengan Policy Laravel
- ✅ Role: **Admin**, **Staff**, **Guest**, **Siswa**
- ✅ Proteksi route dan validasi di setiap endpoint

---

## 🛠️ Tech Stack

| Layer | Teknologi |
|-------|-----------|
| **Backend** | Laravel 12, PHP 8.2+ |
| **Frontend** | Blade Templates, Tailwind CSS, Vite |
| **Database** | MySQL / SQLite |
| **PDF / Barcode** | DomPDF, PHP Barcode Generator, Simple QRCode |
| **Excel** | Maatwebsite Excel (Import/Export) |
| **Image Processing** | Intervention Image |
| **Containerization** | Docker + Docker Compose |
| **Queue** | Laravel Queue (Database Driver) |
| **Caching** | Laravel Cache (File/Redis) |

---

## 🚀 Instalasi

### Prasyarat
- PHP 8.2+
- Composer
- Node.js 18+ & NPM
- MySQL 8+ atau SQLite
- (Opsional) Docker & Docker Compose

---

### ⚡ Install Cepat (1 Perintah)

```bash
composer run setup
```

Perintah ini akan otomatis:
1. Install semua dependency PHP & Node.js
2. Menyalin `.env.example` ke `.env`
3. Generate application key
4. Menjalankan migrasi database
5. Build asset frontend

---

### 🔧 Install Manual (Step by Step)

**1. Clone repositori**
```bash
git clone https://github.com/username/perpustakaan.git
cd perpustakaan
```

**2. Install dependency**
```bash
composer install
npm install
```

**3. Konfigurasi environment**
```bash
cp .env.example .env
php artisan key:generate
```

**4. Konfigurasi database di `.env`**
```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=perpustakaan
DB_USERNAME=root
DB_PASSWORD=
```

**5. Migrasi & seed database**
```bash
php artisan migrate --seed
```

**6. Build frontend**
```bash
npm run build
```

**7. Jalankan server**
```bash
php artisan serve
```

Buka browser ke: **[http://localhost:8000](http://localhost:8000)**

---

### 🐳 Instalasi dengan Docker

```bash
# Clone repository
git clone https://github.com/username/perpustakaan.git
cd perpustakaan

# Jalankan dengan Docker
docker compose up -d

# Masuk ke container dan setup
docker exec -it perpustakaan-app php artisan migrate --seed
```

---

## 👤 Akun Default (Seeder)

Setelah menjalankan `php artisan migrate --seed`, akun berikut tersedia:

| Role | Email | Password |
|------|-------|----------|
| **Admin** | admin@perpustakaan.com | password |
| **Staff** | staff@perpustakaan.com | password |
| **Guest** | guest@perpustakaan.com | password |
| **Siswa** | siswa@perpustakaan.com | password |

> ⚠️ **Ubah password default segera setelah login pertama kali!**

---

## 📁 Struktur Proyek

```
perpustakaan/
├── app/
│   ├── Http/Controllers/     # Semua controller aplikasi
│   ├── Models/               # Model Eloquent (Book, Member, Borrowing, dll.)
│   ├── Policies/             # Aturan akses (RBAC)
│   ├── Services/             # Business logic layer
│   ├── Exports/              # Export Excel
│   └── Imports/              # Import Excel
├── database/
│   ├── migrations/           # Skema database
│   └── seeders/              # Data awal
├── resources/
│   └── views/                # Template Blade
├── routes/
│   └── web.php               # Definisi route
├── docker/                   # Konfigurasi Docker
└── public/                   # Asset publik
```

---

## 🔑 Fitur Role & Akses

| Fitur | Admin | Staff | Guest | Siswa |
|-------|:-----:|:-----:|:-----:|:-----:|
| Dashboard & Statistik | ✅ | ✅ | ✅ | ❌ |
| Manajemen Buku | ✅ | ✅ | ✅ | ❌ |
| Manajemen Anggota | ✅ | ✅ | ✅ | ❌ |
| Proses Peminjaman | ✅ | ✅ | ✅ | ❌ |
| Manajemen Denda | ✅ | ✅ | ❌ | ❌ |
| Laporan & Export | ✅ | ✅ | ❌ | ❌ |
| Pengaturan Sistem | ✅ | ❌ | ❌ | ❌ |
| Manajemen Staff | ✅ | ❌ | ❌ | ❌ |
| Katalog Publik | ✅ | ✅ | ✅ | ✅ |

---

## ⚙️ Konfigurasi Tambahan

### Storage (Foto & PDF)
```bash
php artisan storage:link
```

### Queue Worker (untuk notifikasi & email)
```bash
php artisan queue:work
```

### Cache (untuk performa production)
```bash
php artisan config:cache
php artisan route:cache
php artisan view:cache
```

---

## 📦 Changelog

### v1.0.0 — Rilis Pertama
- ✅ Manajemen buku, anggota, peminjaman, denda
- ✅ Sistem reservasi
- ✅ Import/Export Excel & PDF
- ✅ QR Code & Barcode buku
- ✅ Landing page & katalog publik
- ✅ Role-based access control (4 role)
- ✅ Buku digital (PDF viewer)
- ✅ Gamifikasi: poin & badge anggota
- ✅ Docker support
- ✅ Sistem caching untuk performa optimal

---

## 🤝 Dukungan & Kontribusi

Punya pertanyaan atau menemukan bug? Silakan buka [Issue](https://github.com/username/perpustakaan/issues) di repositori ini.

Ingin berkontribusi? Pull request sangat disambut! Baca [Contributing Guide](CONTRIBUTING.md) terlebih dahulu.

---

## 📄 Lisensi

Proyek ini dilisensikan di bawah [MIT License](LICENSE) — bebas digunakan untuk keperluan pribadi maupun komersial.

---

<div align="center">

**Dibuat dengan ❤️ menggunakan Laravel 12**

⭐ Jika proyek ini bermanfaat, jangan lupa **beri bintang** di GitHub!

</div>
