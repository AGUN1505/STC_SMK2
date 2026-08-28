# 📱 Belajar CSS Responsive & Framework: Web Keren di HP, Tablet, & Laptop! 🚀

Selamat datang di **Pertemuan 5**! 🎉

Pernahkah kamu membuka sebuah website di laptop yang tampilannya sangat rapi, tapi saat dibuka di Smartphone (HP) tampilannya jadi berantakan, teksnya terlalu kecil, atau gambar terpotong? 😱 

Di pertemuan ini, kita akan belajar **rahasia para developer profesional** dalam membuat website yang serba bisa, yaitu **Responsive Web Design**! Selain itu, kita juga akan mengenal **CSS Framework** (Bootstrap & Tailwind CSS) yang membuat proses pembuatan website menjadi 10x lebih cepat dan fleksibel! ⚡

---

## 📚 Daftar Isi
1. 📱 [Apa itu Responsive Web Design (RWD)?](#1-apa-itu-responsive-web-design-rwd)
2. 🔍 [Meta Viewport: Kunci Rahasia Layar HP](#2-meta-viewport-kunci-rahasia-layar-hp)
3. 📐 [Unit Relatif (%, rem, vw/vh) vs Fixed (px)](#3-unit-relatif---rem-vwvh-vs-fixed-px)
4. 🎯 [Media Query: Mantra Ajaib CSS](#4-media-query-mantra-ajaib-css)
5. 🧩 [Breakpoint Layar (Ukuran Standar HP, Tablet, & Laptop)](#5-breakpoint-layar-ukuran-standar-hp-tablet--laptop)
6. ⚡ [Pengenalan CSS Framework](#6-pengenalan-css-framework)
7. 🅰️ [Bootstrap vs 🎨 Tailwind CSS](#7-bootstrap-vs-tailwind-css)
8. 🏗️ [Struktur Layout Website Responsif](#8-struktur-layout-website-responsif)
9. 🎮 [Project Praktek Seru (Hands-On Lab)](#9-project-praktek-seru-hands-on-lab)
   - 🧪 [Praktek 1: Layout Responsif dengan Pure CSS & Media Query](#praktek-1-layout-responsif-dengan-pure-css--media-query)
   - 🅰️ [Praktek 2: Landing Page Kilat dengan Bootstrap 5](#praktek-2-landing-page-kilat-dengan-bootstrap-5)
   - 🎨 [Praktek 3: Kartu Modern dengan Tailwind CSS](#praktek-3-kartu-modern-dengan-tailwind-css)
10. 🎯 [Rangkuman Kilat (Cheat Sheet Pertemuan 5)](#10-rangkuman-kilat-cheat-sheet-pertemuan-5)

---

<a name="1-apa-itu-responsive-web-design-rwd"></a>
## 1. 📱 Apa itu Responsive Web Design (RWD)?

**Responsive Web Design (RWD)** adalah teknik pembuatan website di mana tampilan, ukuran font, gambar, dan tata letak (layout) website **menyesuaikan diri secara otomatis** mengikuti ukuran layar perangkat pengguna.

💡 **Analogi Air dalam Wadah:**
> Air yang dituang ke dalam **gelas** akan berbentuk gelas.
> Air yang dituang ke dalam **botol** akan berbentuk botol.
> Air yang dituang ke dalam **mangkuk** akan berbentuk mangkuk.
> 
> **Website Responsif** seperti air! Tampilannya akan menyesuaikan diri apakah dibaca di **HP kecil**, **Tablet**, **Laptop**, atau **TV Layar Lebar**.

### Mengapa Website Harus Responsif?
1. 📲 **Pengguna HP Sangat Banyak:** Lebih dari 70% pengguna internet mengakses website melalui Smartphone.
2. 👁️ **Kenyamanan Pengguna (UX):** Pengunjung tidak perlu melakukan *zoom in* atau *zoom out* secara manual hanya untuk membaca tulisan.
3. 🥇 **Disukai Google (SEO):** Google lebih memprioritaskan website yang responsif di peringkat atas pencarian.

---

<a name="2-meta-viewport-kunci-rahasia-layar-hp"></a>
## 2. 🔍 Meta Viewport: Kunci Rahasia Layar HP

Sebelum menulis kode CSS responsif, ada **satu baris kode HTML WAJIB** yang harus ada di dalam tag `<head>`. Tanpa tag ini, browser HP akan menganggap websitemu adalah versi desktop dan akan memperkecil tampilan seluruh halaman sampai teks tidak terbaca!

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Bedah Kode Meta Viewport:
* `name="viewport"`: Meminta browser mengatur area tampilan (viewport).
* `width=device-width`: Mengatur lebar area kerja agar sama persis dengan lebar layar HP/perangkat pengguna.
* `initial-scale=1.0`: Mengatur tingkat zoom awal sebesar 100% (ukuran normal).

---

<a name="3-unit-relatif---rem-vwvh-vs-fixed-px"></a>
## 3. 📐 Unit Relatif (%, rem, vw/vh) vs Fixed (px)

Dalam CSS Responsif, hindari menentukan ukuran layout utama dengan satuan kaku (absolut) seperti Pixel (`px`) secara berlebihan. Gunakan **Unit Relatif** agar elemen bisa membesar dan mengecil secara fleksibel!

| Satuan | Jenis | Penjelasan & Cara Kerja | Kapan Digunakan? |
| :--- | :--- | :--- | :--- |
| `px` (Pixel) | **Absolut** | Ukuran kaku/tetap. 100px akan selalu 100px di layar HP maupun TV. | Border, shadow, padding kecil. |
| `%` (Persentase) | **Relatif** | Ukuran dihitung berdasarkan ukuran **elemen induk (parent)**. | Lebar kolom layout, wadah/container. |
| `rem` | **Relatif** | Ukuran dihitung berdasarkan font dasar browser (`<html>`). Standar 1rem = 16px. | Ukuran font (`font-size`), margin, padding. |
| `vw` (Viewport Width) | **Relatif** | 1vw = 1% dari total **lebar layar browser**. | Hero header, judul besar yang fleksibel. |
| `vh` (Viewport Height) | **Relatif** | 1vh = 1% dari total **tinggi layar browser**. | Section full-screen (100vh). |

### 💡 Contoh Perbandingan Kode:
```css
/* ❌ Kurang Fleksibel (Kaku): */
.kotak-kaku {
    width: 800px; /* Jika dibuka di HP yang lebarnya 360px, akan jebol ke kanan! */
}

/* ✅ Responsif (Fleksibel): */
.kotak-fleksibel {
    width: 90%; /* Selalu mengambil 90% dari lebar layar */
    max-width: 800px; /* Tapi tidak boleh lebih besar dari 800px di PC */
}
```

---

<a name="4-media-query-mantra-ajaib-css"></a>
## 4. 🎯 Media Query: Mantra Ajaib CSS

**Media Query** adalah fitur CSS yang memungkinkan kita memberikan perintah/gaya CSS tertentu **hanya jika** syarat ukuran layar terpenuhi.

### Syntax / Rumus Dasar Media Query:
```css
@media screen and (max-width: 768px) {
    /* 
       Kode CSS di dalam sini HANYA akan berjalan 
       jika lebar layar KURANG DARI ATAU SAMA DENGAN 768px (HP/Tablet)
    */
    body {
        background-color: lightblue;
    }
}
```

### 💡 Analogi Media Query:
> *"Hei Browser! Kalau layar pengguna lebar (Laptop), tampilkan menu navigasi di atas secara mendatar. Tapi **JIKA (Media Query)** layar pengguna kurang dari 768px (HP), ubah menu jadi menumpuk ke bawah atau munculkan tombol burger!"*

---

<a name="5-breakpoint-layar-ukuran-standar-hp-tablet--laptop"></a>
## 5. 🧩 Breakpoint Layar (Ukuran Standar HP, Tablet, & Laptop)

**Breakpoint** adalah titik batas ukuran layar di mana tampilan website mulai berubah tata letaknya.

Berikut adalah ukuran standar breakpoint yang sering digunakan di industri:

```
📱 Mobile (HP)            : < 576px       (Layar HP Tegak)
📱 Mobile Large / Tablet  : 576px - 768px (HP Lanskap / Tablet Kecil)
💻 Tablet / Laptop Kecil  : 768px - 992px (Tablet Tegak / iPad)
🖥️ Desktop / Laptop Besar : 992px - 1200px (Laptop 14", PC Monitor)
🖥️ Large Desktop (TV)    : > 1200px      (Monitor Besar / 4K)
```

### Contoh Kode Breakpoint Sederhana:
```css
/* Tampilan Dasar (Desktop / Default) */
.wadah-kartu {
    display: flex;
    flex-direction: row; /* Kolom sejajar menyamping di PC */
}

/* Ketiuka Layar HP (Kurang dari 768px) */
@media screen and (max-width: 768px) {
    .wadah-kartu {
        flex-direction: column; /* Ubah jadi menumpuk ke bawah di HP */
    }
}
```

---

<a name="6-pengenalan-css-framework"></a>
## 6. ⚡ Pengenalan CSS Framework

Membangun website responsif dari nol menggunakan Pure CSS sangat bagus untuk melatih logika. Namun, di dunia kerja, para developer menggunakan **CSS Framework** untuk mempercepat pekerjaan!

### Apa itu CSS Framework?
**CSS Framework** adalah kumpulan kode CSS siap pakai yang telah dibuat oleh tim developer ahli. Kamu tinggal memanggil class-class yang sudah disediakan tanpa harus menulis kode CSS dari nol!

### Keuntungan Pakai Framework:
* 🚀 **Sangat Cepat:** Tidak perlu buat sistem Grid atau Media Query sendiri.
* 📱 **Sudah Otomatis Responsif:** Komponen langsung menyesuaikan layar.
* 🎨 **Desain Konsisten:** Memiliki standar warna, tombol, dan font yang rapi.

---

<a name="7-bootstrap-vs-tailwind-css"></a>
## 7. 🅰️ Bootstrap vs 🎨 Tailwind CSS

Dua framework CSS paling populer saat ini adalah **Bootstrap** dan **Tailwind CSS**. Keduanya hebat, tapi cara kerjanya berbeda!

```
                    ┌─────────────────────────┐
                    │     CSS FRAMEWORK       │
                    └────────────┬────────────┘
                                 │
                 ┌───────────────┴───────────────┐
                 ▼                               ▼
    🅰️ BOOTSTRAP                      🎨 TAILWIND CSS
 (Component-Based Framework)            (Utility-First Framework)
 - Seperti main LEGO siap jadi.          - Seperti main balok tanah liat.
 - Tombol, Navbar, Card sudah jadi.      - Kamu racik sendiri class kecilnya.
```

### Perbandingan Singkat:

| Fitur | 🅰️ Bootstrap 5 | 🎨 Tailwind CSS |
| :--- | :--- | :--- |
| **Pendekatan** | **Component-First** (Komponen Siap Pakai) | **Utility-First** (Class Utility Spesifik) |
| **Kemudahan** | ⭐⭐⭐⭐⭐ (Sangat Mudah untuk Pemula) | ⭐⭐⭐⭐ (Butuh hapal class utility) |
| **Kecepatan Buat** | Sangat Cepat (Tinggal copy component) | Cepat & Sangat Fleksibel |
| **Kebebasan Desain** | Tampilan cenderung mirip web Bootstrap lain | Bebas 100% sesuai imajinasimu |
| **Contoh Tombol** | `<button class="btn btn-primary">` | `<button class="bg-blue-500 text-white p-2 rounded">` |

---

<a name="8-struktur-layout-website-responsif"></a>
## 8. 🏗️ Struktur Layout Website Responsif

Anatomi standar sebuah halaman web yang responsif terdiri dari 5 bagian utama:

```
┌───────────────────────────────────────────────────────────┐
│ 1. NAVBAR / HEADER (Logo + Menu Navigasi)                │
├───────────────────────────────────────────────────────────┤
│ 2. HERO SECTION (Banner Utama + Tombol Aksi / CTA)        │
├─────────────────────────────────────────────┬─────────────┤
│ 3. MAIN CONTENT (Artikel / Produk / Grid)   │ 4. SIDEBAR  │
│ (Desktop: 2-3 Kolom | HP: Menumpuk 1 Kolom) │             │
├─────────────────────────────────────────────┴─────────────┤
│ 5. FOOTER (Hak Cipta & Link Sosial Media)                 │
└───────────────────────────────────────────────────────────┘
```

---

<a name="9-project-praktek-seru-hands-on-lab"></a>
## 9. 🎮 Project Praktek Seru (Hands-On Lab)

Sekarang saatnya kita coba praktek langsung! Kita akan membagi praktek menjadi 3 bagian:
1. **Praktek 1:** Membuat Layout Responsif dengan Pure CSS & Media Query.
2. **Praktek 2:** Membuat Landing Page Instan menggunakan **Bootstrap 5**.
3. **Praktek 3:** Membuat Kartu Produk Modern menggunakan **Tailwind CSS**.

---

<a name="praktek-1-layout-responsif-dengan-pure-css--media-query"></a>
### 🧪 Praktek 1: Layout Responsif dengan Pure CSS & Media Query

Mari buat halaman berita sederhana dengan 3 kolom di Laptop, tapi otomatis menjadi 1 kolom di HP!

#### 📄 Kode HTML: `praktek1.html`
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <!-- Meta Viewport WAJIB! -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Praktek 1: Pure CSS Responsive</title>
    <link rel="stylesheet" href="style1.css">
</head>
<body>

    <header class="header">
        <h1>🌐 Portal Berita Teknologi</h1>
        <p>Berita IT Terupdate Setiap Hari</p>
    </header>

    <div class="container">
        <!-- Wadah Utama Flexbox -->
        <main class="grid-berita">
            
            <article class="kartu-berita">
                <span class="tag">AI</span>
                <h3>Kecerdasan Buatan Semakin Canggih</h3>
                <p>Teknologi AI kini membantu para siswa belajar koding lebih mudah dan menyenangkan.</p>
            </article>

            <article class="kartu-berita">
                <span class="tag">WEB</span>
                <h3>Framework CSS Terpopuler 2026</h3>
                <p>Tailwind dan Bootstrap masih menjadi pilihan utama para developer dunia.</p>
            </article>

            <article class="kartu-berita">
                <span class="tag">GADGET</span>
                <h3>HP Masa Depan Layar Lipat</h3>
                <p>Inovasi layar lipat semakin tipis dengan daya tahan baterai hingga 3 hari.</p>
            </article>

        </main>
    </div>

</body>
</html>
```

#### 🎨 Kode CSS: `style1.css`
```css
/* 1. Reset Dasar */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    background-color: #f1f5f9;
    color: #334155;
}

/* 2. Header */
.header {
    background-color: #0f172a;
    color: white;
    text-align: center;
    padding: 30px 20px;
}

.header h1 {
    margin-bottom: 5px;
}

/* 3. Layout Grid Berita (Tampilan Laptop / PC) */
.container {
    max-width: 1100px;
    margin: 30px auto;
    padding: 0 20px;
}

.grid-berita {
    display: flex;
    gap: 20px; /* Jarak antar kartu */
    justify-content: space-between;
}

.kartu-berita {
    background-color: white;
    flex: 1; /* Setiap kartu membagi lebar secara adil (3 kolom) */
    padding: 20px;
    border-radius: 12px;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
    border-top: 4px solid #3b82f6;
}

.tag {
    background-color: #eff6ff;
    color: #2563eb;
    padding: 4px 10px;
    font-size: 12px;
    font-weight: bold;
    border-radius: 6px;
}

.kartu-berita h3 {
    margin: 15px 0 10px 0;
    color: #1e293b;
}

/* =================================================== */
/* 4. MEDIA QUERY: RESPONSIF UNTUK HP (Layar <= 768px) */
/* =================================================== */
@media screen and (max-width: 768px) {
    .grid-berita {
        flex-direction: column; /* Ubah susunan dari menyamping jadi menumpuk ke bawah! */
    }

    .header {
        padding: 20px 10px;
    }

    .header h1 {
        font-size: 22px;
    }
}
```

---

<a name="praktek-2-landing-page-kilat-dengan-bootstrap-5"></a>
### 🅰️ Praktek 2: Landing Page Kilat dengan Bootstrap 5

Di praktek ini, kita tidak perlu membuat file CSS terpisah! Cukup hubungkan CDN Bootstrap 5 dan gunakan class bawaannya.

#### 📄 Kode HTML: `bootstrap_demo.html`
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Praktek 2: Bootstrap 5 Landing Page</title>
    <!-- CDN Bootstrap 5 CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body class="bg-light">

    <!-- 1. NAVBAR RESPONSIF BOOTSTRAP -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container">
            <a class="navbar-brand fw-bold" href="#">🚀 KodingAcademy</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link active" href="#">Home</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Kelas</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Tentang</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Kontak</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- 2. HERO SECTION -->
    <section class="container my-5 text-center">
        <div class="p-5 bg-primary text-white rounded-3 shadow">
            <h1 class="display-4 fw-bold">Belajar Web Design Mudah & Seru!</h1>
            <p class="lead">Kuasai HTML, CSS, Responsive Design, hingga Framework modern bersama kami.</p>
            <a href="#" class="btn btn-warning btn-lg fw-bold mt-3">Daftar Sekarang 🚀</a>
        </div>
    </section>

    <!-- 3. GRID KARTU KELAS (RESPONSIF BOOTSTRAP) -->
    <section class="container mb-5">
        <h2 class="text-center mb-4 fw-bold">Pilihan Kelas</h2>
        
        <!-- row-cols-1 di HP, row-cols-md-3 di Tablet/PC -->
        <div class="row row-cols-1 row-cols-md-3 g-4">
            
            <div class="col">
                <div class="card h-100 shadow-sm border-0">
                    <div class="card-body">
                        <h5 class="card-title fw-bold text-primary">HTML & CSS Dasar</h5>
                        <p class="card-text">Pelajari fondasi utama dalam membangun struktur dan gaya halaman web.</p>
                        <button class="btn btn-outline-primary w-100">Lihat Detail</button>
                    </div>
                </div>
            </div>

            <div class="col">
                <div class="card h-100 shadow-sm border-0">
                    <div class="card-body">
                        <h5 class="card-title fw-bold text-success">Responsive & Grid</h5>
                        <p class="card-text">Buat websitemu tampil sempurna di Smartphone, Tablet, dan Desktop.</p>
                        <button class="btn btn-outline-success w-100">Lihat Detail</button>
                    </div>
                </div>
            </div>

            <div class="col">
                <div class="card h-100 shadow-sm border-0">
                    <div class="card-body">
                        <h5 class="card-title fw-bold text-danger">Bootstrap 5 Master</h5>
                        <p class="card-text">Membangun website profesional secara cepat dengan komponen Bootstrap.</p>
                        <button class="btn btn-outline-danger w-100">Lihat Detail</button>
                    </div>
                </div>
            </div>

        </div>
    </section>

    <!-- FOOTER -->
    <footer class="bg-dark text-white text-center py-3">
        <p class="m-0">&copy; 2026 KodingAcademy. All Rights Reserved.</p>
    </footer>

    <!-- CDN Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

---

<a name="praktek-3-kartu-modern-dengan-tailwind-css"></a>
### 🎨 Praktek 3: Kartu Modern dengan Tailwind CSS

Sekarang mari kita coba menggunakan **Tailwind CSS** melalui CDN Script.

#### 📄 Kode HTML: `tailwind_demo.html`
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Praktek 3: Tailwind CSS Card</title>
    <!-- CDN Tailwind CSS CDN Play -->
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-slate-900 min-h-screen flex items-center justify-center p-5">

    <!-- KARTU MODERN TAILWIND -->
    <div class="max-w-sm w-full bg-slate-800 rounded-2xl p-6 shadow-2xl border border-slate-700 text-white transform transition hover:-translate-y-2 hover:shadow-cyan-500/20">
        
        <!-- Badge -->
        <div class="flex justify-between items-center mb-4">
            <span class="bg-cyan-500/10 text-cyan-400 text-xs font-semibold px-3 py-1 rounded-full border border-cyan-500/30">
                Tailwind CSS
            </span>
            <span class="text-slate-400 text-xs">Pertemuan 5</span>
        </div>

        <!-- Judul & Deskripsi -->
        <h3 class="text-xl font-bold mb-2 text-slate-100">Utility-First Framework</h3>
        <p class="text-slate-400 text-sm leading-relaxed mb-6">
            Dengan Tailwind CSS, kamu bisa meracik desain komponen secara fleksibel langsung dari class HTML tanpa meninggalkan file!
        </p>

        <!-- Statistik Keren -->
        <div class="grid grid-cols-2 gap-4 bg-slate-900/60 p-3 rounded-xl mb-6 border border-slate-800">
            <div class="text-center">
                <p class="text-xs text-slate-400">Kecepatan</p>
                <p class="text-lg font-bold text-cyan-400">10x Lebih Cepat</p>
            </div>
            <div class="text-center">
                <p class="text-xs text-slate-400">Kustomisasi</p>
                <p class="text-lg font-bold text-emerald-400">100% Bebas</p>
            </div>
        </div>

        <!-- Tombol Aksi -->
        <button class="w-full bg-gradient-to-r from-cyan-500 to-blue-600 hover:from-cyan-600 hover:to-blue-700 text-white font-bold py-3 rounded-xl shadow-lg shadow-cyan-500/30 transition duration-300">
            Pelajari Sekarang ✨
        </button>
    </div>

</body>
</html>
```

---

<a name="10-rangkuman-kilat-cheat-sheet-pertemuan-5"></a>
## 10. 🎯 Rangkuman Kilat (Cheat Sheet Pertemuan 5) 🧠

| Konsep / Istilah | Kunci Rahasia / Fungsi Utama | Contoh Kode |
| :--- | :--- | :--- |
| **Meta Viewport** | Wajib di tag `<head>` agar layar HP tidak zoom-out otomatis | `<meta name="viewport" content="width=device-width, initial-scale=1.0">` |
| **Media Query** | Memberikan aturan CSS khusus berdasarkan ukuran layar | `@media screen and (max-width: 768px) { ... }` |
| **Max-Width vs Min-Width** | `max-width` = Desktop-First (HP diubah)<br>`min-width` = Mobile-First (Laptop diubah) | `max-width: 768px` |
| **Unit Relatif** | Satuan fleksibel untuk membuat elemen responsif | `width: 100%`, `font-size: 1.5rem`, `height: 100vh` |
| **Bootstrap 5** | Framework komponen siap pakai (`btn`, `card`, `row`, `col`) | `<div class="col-md-4 card">` |
| **Tailwind CSS** | Framework utility-first untuk kustomisasi bebas & cepat | `<div class="flex flex-col md:flex-row p-4">` |

---

### 🎉 Selamat!
Kamu telah menyelesaikan materi **Pertemuan 5: CSS Responsive & Framework**! Sekarang kamu sudah bisa membuat website modern yang tampil keren di semua perangkat (HP, Tablet, maupun Laptop)! 🚀💻📱
