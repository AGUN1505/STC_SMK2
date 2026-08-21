# 🎨 Belajar CSS Dasar: Menghias Halaman Web Jadi Keren dan Seru! 🚀

Selamat datang di dunia **CSS**! 

Kalau **HTML** adalah tulang dan struktur dari halaman web (seperti dinding dan atap rumah), maka **CSS** adalah cat warna, wallpaper, hiasan, dan tata letak perabotannya. Tanpa CSS, halaman web hanya akan berisi teks hitam-putih yang membosankan. Dengan CSS, kamu bisa jadi seorang desainer digital! 🎨✨

---

## 📚 Daftar Isi
1. 🏠 [Apa itu CSS?](#1-apa-itu-css)
2. 🎯 [Selector: Memilih Elemen yang Mau Dihias](#2-selector-memilih-elemen-yang-mau-dihias)
3. 🎨 [Color (Warna): Memberi Warna pada Web](#3-color-warna-memberi-warna-pada-web)
4. 🔤 [Font & Teks: Mengubah Gaya Tulisan](#4-font--teks-mengubah-gaya-tulisan)
5. 📦 [Margin & Padding: Mengatur Jarak (Box Model Bagian 1)](#5-margin--padding-mengatur-jarak-box-model-bagian-1)
6. 🖼️ [Border: Membuat Bingkai & Pagar](#6-border-membuat-bingkai--pagar)
7. 🧱 [Display: Cara Elemen Muncul di Layar](#7-display-cara-elemen-muncul-di-layar)
8. 🧩 [Flexbox: Kotak Ajaib Penyusun Tata Letak](#8-flexbox-kotak-ajaib-penyusun-tata-letak)
9. 🎮 [Project Seru: Kartu Karakter Game Ajaib!](#9-project-seru-kartu-karakter-game-ajaib)

---

<a name="1-apa-itu-css"></a>
## 1. 🏠 Apa itu CSS?

**CSS** singkatan dari *Cascading Style Sheets*. 

💡 **Analogi Mudah:**
* **HTML** = Mobil polos tanpa cat, belum ada bangku empuk, belum ada stiker.
* **CSS** = Cat merah mengkilap, stiker api yang keren, dan jok kulit yang empuk!

### Cara Menulis CSS:
Struktur penulisan CSS sangat sederhana:

```css
target-elemen {
    properti: nilai;
}
```

* **Target (Selector):** Elemen apa yang mau disapa/dihias? (Contoh: `h1`, `p`, `button`)
* **Properti:** Apa yang mau diubah? (Contoh: `color`, `font-size`, `background-color`)
* **Nilai:** Seperti apa perubahannya? (Contoh: `red`, `20px`, `blue`)

---

<a name="2-selector-memilih-elemen-yang-mau-dihias"></a>
## 2. 🎯 Selector: Memilih Elemen yang Mau Dihias

Bayangkan kamu adalah seorang guru di kelas. Kamu mau memanggil murid-muridmu. Kamu punya beberapa cara untuk memanggil mereka:

1. **Memanggil SEMUA murid:** "Semua murid, berdiri!" *(Universal Selector)*
2. **Memanggil berdasarkan JENIS:** "Semua yang pakai baju merah, maju!" *(Element Selector)*
3. **Memanggil KELOMPOK KHUSUS:** "Anggota Klub Melukis, kumpul!" *(Class Selector)*
4. **Memanggil SATU ORANG KHUSUS:** "Budi yang punya nomor induk 001, maju!" *(ID Selector)*

Di CSS, cara kerjanya persis seperti itu!

---

### A. Element Selector (Berdasarkan Tag HTML)
Memilih **semua** tag yang sejenis.

```css
/* Mengubah SEMUA judul h1 menjadi biru */
h1 {
    color: blue;
}

/* Mengubah SEMUA paragraf menjadi ukuran 18px */
p {
    font-size: 18px;
}
```

---

### B. Class Selector (Berdasarkan Kelompok) ⭐️ *Paling Sering Dipakai!*
Digunakan untuk memberi gaya pada elemen-elemen tertentu saja. Di HTML memakai `class="..."`, dan di CSS diawali dengan tanda **titik (`.`)**.

**HTML:**
```html
<p class="pesan-penting">Ini peringatan rahasia!</p>
<p>Ini paragraf biasa saja.</p>
```

**CSS:**
```css
/* Hanya elemen dengan class "pesan-penting" yang berwarna merah */
.pesan-penting {
    color: red;
    font-weight: bold;
}
```

---

### C. ID Selector (Berdasarkan Identitas Unik)
Digunakan untuk **satu** elemen yang sangat spesial dan tidak ada kembarannya di satu halaman. Di HTML memakai `id="..."`, dan di CSS diawali dengan tanda **pagar (`#`)**.

**HTML:**
```html
<button id="tombol-super">Klik Tombol Super!</button>
```

**CSS:**
```css
#tombol-super {
    background-color: gold;
    color: black;
}
```

---

### D. Universal Selector & Grouping Selector

* **Universal Selector (`*`):** Memilih SEMUA elemen di halaman.
  ```css
  * {
      margin: 0;
      padding: 0;
  }
  ```

* **Grouping Selector (Koma `,`):** Memilih beberapa elemen sekaligus agar tidak perlu nulis berulang-ulang.
  ```css
  h1, h2, h3 {
      font-family: Arial, sans-serif;
      color: darkblue;
  }
  ```

---

<a name="3-color-warna-memberi-warna-pada-web"></a>
## 3. 🎨 Color (Warna): Memberi Warna pada Web

Di CSS, kita bisa mewarnai **teks** (`color`) dan **latar belakang** (`background-color`).

```css
h1 {
    color: white;                   /* Warna teks */
    background-color: deepskyblue;  /* Warna latar belakang */
}
```

---

### 🖌️ 3 Cara Menyebutkan Warna di CSS:

#### 1. Nama Warna (Named Colors)
CSS punya 140+ nama warna siap pakai!
* Contoh: `red`, `blue`, `green`, `orange`, `gold`, `crimson`, `purple`, `skyblue`, `tomato`, `pink`.

```css
p {
    color: tomato;
}
```

#### 2. Kode HEX (Hexadecimal)
Kode unik diawali tanda `#` dan 6 karakter (kombinasi angka & huruf).
* `#FF0000` = Merah
* `#00FF00` = Hijau
* `#0000FF` = Biru
* `#000000` = Hitam
* `#FFFFFF` = Putih

```css
body {
    background-color: #f0f8ff;
}
```

#### 3. RGB & RGBA (Red, Green, Blue, Alpha)
Menggabungkan kadar warna Merah (R), Hijau (G), dan Biru (B) dari angka 0 sampai 255. 
Huruf **A** (Alpha) digunakan untuk membuat warna **transparan/tembus pandang** (0 = transparan total, 1 = pekat).

```css
/* Merah pekat */
div {
    background-color: rgb(255, 0, 0);
}

/* Biru agak transparan (kaca) */
.kotak-kaca {
    background-color: rgba(0, 0, 255, 0.5);
}
```

---

<a name="4-font--teks-mengubah-gaya-tulisan"></a>
## 4. 🔤 Font & Teks: Mengubah Gaya Tulisan

Tulisan di komputer bisa kita atur jenisnya, ukurannya, tebalnya, dan kerapihannya!

```css
.tulisan-keren {
    font-family: 'Poppins', Arial, sans-serif; /* Jenis Font */
    font-size: 20px;                            /* Ukuran Tulisan */
    font-weight: bold;                          /* Ketebalan (normal/bold/100-900) */
    font-style: italic;                         /* Miring */
    text-align: center;                         /* Posisi teks: left, center, right, justify */
    line-height: 1.6;                           /* Jarak antar baris kalimat */
    text-decoration: underline;                 /* Garis bawah / line-through (coret) */
}
```

### 💡 Tips Memilih Font:
1. **Sans-Serif (Modern & Bersih):** Contoh: Arial, Helvetica, Verdana. Sangat cocok untuk dibaca di layar HP/Komputer.
2. **Serif (Klasik & Resmi):** Contoh: Times New Roman, Georgia. Punya "kaki" kecil di setiap hurufnya seperti di buku novel.
3. **Monospace (Gaya Kode/Ketik):** Contoh: Courier New, Consolas. Setiap huruf lebarnya sama persis.

---

<a name="5-margin--padding-mengatur-jarak-box-model-bagian-1"></a>
## 5. 📦 Margin & Padding: Mengatur Jarak (Box Model Bagian 1)

Setiap elemen di HTML sebenarnya berbentuk seperti **Kotak (Box)**. Untuk mengatur posisi kotak tersebut, kita mengenal dua istilah penting: **Margin** dan **Padding**.

💡 **Analogi Super Mudah:**
* **Padding:** Busa empuk di **dalam** kotak kado / jarak dari baju ke kulitmu. (Jarak di DALAM batas elemen).
* **Margin:** Jarak **luar** antara kotak kado dengan kotak kado lainnya di sekitarnya. (Jarak di LUAR batas elemen).

---

### 📐 Visualisasi Box Model:

```text
+-------------------------------------------------------+
|                       MARGIN                          |
|   +-----------------------------------------------+   |
|   |                   BORDER                      |   |
|   |   +---------------------------------------+   |   |
|   |   |               PADDING                 |   |   |
|   |   |   +-------------------------------+   |   |   |
|   |   |   |      KONTEN (Teks/Gambar)     |   |   |   |
|   |   |   +-------------------------------+   |   |   |
|   |   +---------------------------------------+   |   |
|   +-----------------------------------------------+   |
+-------------------------------------------------------+
```

---

### Contoh Penulisan Margin & Padding:

```css
.kotak {
    /* Menentukan jarak satu per satu */
    padding-top: 10px;      /* Atas */
    padding-right: 15px;    /* Kanan */
    padding-bottom: 10px;   /* Bawah */
    padding-left: 15px;     /* Kiri */

    margin-top: 20px;
    margin-bottom: 20px;
}
```

### 🚀 Cara Cepat (Shorthand):
Kamu bisa menuliskan 4 arah sekaligus berurutan searah jarum jam: **Atas ➡️ Kanan ➡️ Bawah ➡️ Kiri** (Ingat: **A-K-B-K**).

```css
/* Atas(10px) Kanan(20px) Bawah(10px) Kiri(20px) */
.kotak {
    padding: 10px 20px 10px 20px;
}

/* Kalau Atas-Bawah sama, Kanan-Kiri sama (2 nilai): */
/* 10px = Atas & Bawah, 20px = Kanan & Kiri */
.kotak {
    margin: 10px 20px;
}

/* Kalau keempat sisinya sama persis (1 nilai): */
.kotak {
    padding: 15px;
}
```

✨ **Triks Rahasia!** Biar kotakmu berada di tengah-tengah layar secara horizontal:
```css
.kotak-tengah {
    width: 300px;
    margin: 0 auto; /* Atas-Bawah 0, Kanan-Kiri Otomatis Tengah! */
}
```

---

<a name="6-border-membuat-bingkai--pagar"></a>
## 6. 🖼️ Border: Membuat Bingkai & Pagar

**Border** adalah pagar atau garis bingkai yang membungkus isi elemen.

```css
.kartu {
    border-width: 3px;          /* Ketebalan garis */
    border-style: solid;        /* Bentuk garis: solid, dashed, dotted, double */
    border-color: dodgerblue;   /* Warna garis */
}
```

---

### 🚀 Cara Cepat Menulis Border (3-in-1):
Cukup tulis `border: [tebal] [gaya] [warna];`

```css
.kartu-1 {
    border: 2px solid black;      /* Garis lurus biasa */
}

.kartu-2 {
    border: 3px dashed red;       /* Garis putus-putus */
}

.kartu-3 {
    border: 4px dotted green;     /* Garis titik-titik */
}
```

---

### 🟡 Border Radius (Sudut Membulat!)
Bosan dengan kotak yang sudutnya lancip? Pakai `border-radius` agar sudutnya melengkung halus seperti kartu modern!

```css
.kartu-modern {
    border: 2px solid purple;
    border-radius: 15px; /* Makin besar angkanya, makin bulat sudutnya! */
}

/* Trik membuat lingkaran sempurna: */
.foto-profil {
    width: 100px;
    height: 100px;
    border-radius: 50%; /* 50% akan mengubah kotak jadi lingkaran! */
}
```

---

<a name="7-display-cara-elemen-muncul-di-layar"></a>
## 7. 🧱 Display: Cara Elemen Muncul di Layar

Sifat dasar elemen di HTML terbagi menjadi dua kelompok besar saat tampil di layar:

### 1. `display: block;`
* Suka **maruk tempat**! Dia akan mengambil 100% lebar layar dari kiri ke kanan.
* Elemen berikutnya pasti terlempar ke **baris baru di bawahnya**.
* Contoh bawaan: `<h1>`, `<p>`, `<div>`, `<ul>`.

```text
[      Elemen Block 1 (Menguasai 1 Baris Penuh)      ]
[      Elemen Block 2 (Menguasai 1 Baris Penuh)      ]
```

### 2. `display: inline;`
* Hemat tempat! Lebarnya **pas mengikuti isi tulisan/kontennya saja**.
* Elemen lain bisa duduk berjejer **di sampingnya** dalam 1 baris.
* ⚠️ *Catatan:* Tidak bisa diatur `width` (lebar) dan `height` (tinggi)-nya.
* Contoh bawaan: `<span>`, `<a>`, `<b>`, `<i>`.

```text
[Inline 1] [Inline 2] [Inline 3]
```

---

### 3. `display: inline-block;`
* Gabungan keunggulan keduanya! Bisa berjejer ke samping (seperti *inline*), **TAPI** lebarnya dan tingginya tetap bisa diatur (seperti *block*).
* Sangat cocok untuk membuat **Tombol (Button)** atau **Menu Navigasi**!

```css
.tombol-menu {
    display: inline-block;
    width: 120px;
    height: 40px;
    background-color: orange;
}
```

---

### 4. `display: none;`
* Menghilangkan elemen dari layar secara total (seperti sulapilusi/menghilang!). Elemen tidak akan terlihat dan tidak memakan tempat sama sekali.

```css
.pesan-tersembunyi {
    display: none;
}
```

---

<a name="8-flexbox-kotak-ajaib-penyusun-tata-letak"></a>
## 8. 🧩 Flexbox: Kotak Ajaib Penyusun Tata Letak

**Flexbox** (Flexible Box) adalah fitur CSS super canggih yang membuat proses menyusun elemen jadi **mudah, rapi, dan responsif**!

💡 **Analogi:** Bayangkan kamu punya rak mainan ajaib (`display: flex`). Apapun mainan yang kamu masukkan ke dalamnya, bisa kamu perintahkan: *"Semua mainan, berbaris di tengah!"* atau *"Kumpul di sebelah kanan!"* secara otomatis!

---

### A. Mengaktifkan Flexbox
Flexbox dipasang pada elemen pembungkusnya (Parent/Wadah).

```css
.wadah-mainan {
    display: flex;
}
```

Begitu kamu memberi `display: flex`, semua anak di dalamnya (*flex items*) akan langsung berjejer rapi ke samping!

---

### B. Properti Utama Flexbox:

#### 1. `flex-direction` (Arah Barisan)
Menentukan anak-anaknya mau berbaris ke samping atau ke bawah.
* `row` (Default): Ke samping dari kiri ke kanan.
* `column`: Ke bawah seperti tumpukan balok.

```css
.wadah-mainan {
    display: flex;
    flex-direction: row; /* atau column */
}
```

---

#### 2. `justify-content` (Meratakan Posisi Horizontal / Sumbu Utama)
Mengatur posisi anak-anaknya di sepanjang barisan.

* `flex-start`: Kumpul di sebelah kiri (awal).
* `center`: Kumpul pas di **tengah-tengah**! 🎯
* `flex-end`: Kumpul di sebelah kanan (akhir).
* `space-between`: Menyebar dengan jarak sama rata, anak pertama di pojok kiri & anak terakhir di pojok kanan.
* `space-around`: Menyebar rapi dengan memberi ruang kosong seimbang di sekeliling tiap anak.

```text
flex-start   : [A][B][C]-----------------
center       : ---------Wait[A][B][C]--------
flex-end     : -----------------[A][B][C]
space-between: [A]--------- [B] ---------[C]
```

```css
.wadah-pilihan {
    display: flex;
    justify-content: space-between;
}
```

---

#### 3. `align-items` (Meratakan Posisi Vertikal / Sumbu Tegak)
Mengatur posisi anak secara tegak lurus (atas-bawah).

* `stretch` (Default): Menarik anak agar tingginya memenuhi wadah.
* `center`: Membuat semua anak berada di **tengah-tengah tinggi wadah**!
* `flex-start`: Mepet ke atas.
* `flex-end`: Mepet ke bawah.

---

### 🌟 Trik Paling Populer di Dunia Web:
Cara membuat sebuah elemen berada **pas di tengah-tengah layar** (Tengah Horizontal & Tengah Vertikal):

```css
.wadah-tengah-sempurna {
    display: flex;
    justify-content: center; /* Tengah Kiri-Kanan */
    align-items: center;     /* Tengah Atas-Bawah */
    height: 100vh;           /* Tinggi selayar penuh */
}
```

---

#### 4. `gap` (Jarak Antar Anak)
Membuat jarak antar anak tanpa perlu ribet memberi margin satu per satu.

```css
.wadah-mainan {
    display: flex;
    gap: 20px; /* Jarak antar item 20 pixel */
}
```

---

<a name="9-project-seru-kartu-karakter-game-ajaib"></a>
## 9. 🎮 Project Seru: Kartu Karakter Game Ajaib!

Yuk gabungkan semua ilmu CSS yang sudah kita pelajari untuk membuat **Kartu Profil Pahlawan Super / Karakter Game**!

### 📝 Salin Kode HTML Ini: `index.html`

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kartu Karakter Game</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Wadah Utama Flexbox untuk menaruh kartu di tengah layar -->
    <div class="layar-utama">

        <!-- Kartu Karakter -->
        <div class="kartu-karakter">
            <div class="lencana-level">LVL 99</div>
            <img src="https://api.dicebear.com/7.x/bottts/svg?seed=RobotHero" alt="Avatar Robot" class="foto-karakter">
            <h2 class="nama-karakter">Robo-X 3000</h2>
            <p class="tipe-karakter">Penjaga Galaksi Cyber</p>
            
            <!-- Statistik Keterampilan -->
            <div class="wadah-stats">
                <div class="stat-box">
                    <span class="angka-stat">⚡ 95</span>
                    <span class="label-stat">Speed</span>
                </div>
                <div class="stat-box">
                    <span class="angka-stat">🛡️ 88</span>
                    <span class="label-stat">Armor</span>
                </div>
                <div class="stat-box">
                    <span class="angka-stat">🔥 99</span>
                    <span class="label-stat">Power</span>
                </div>
            </div>

            <!-- Tombol Aksi -->
            <button class="tombol-main">Pilih Pahlawan</button>
        </div>

    </div>

</body>
</html>
```

---

### 🎨 Salin Kode CSS Ini: `style.css`

```css
/* 1. Reset & Font Dasar */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

/* 2. Mewarnai Latar Belakang & Menaruh Kartu di Tengah Layar dengan Flexbox */
.layar-utama {
    background-color: #0f172a;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

/* 3. Menghias Kartu Utama */
.kartu-karakter {
    background-color: #1e293b;
    width: 320px;
    padding: 25px;
    border-radius: 20px;
    border: 3px solid #38bdf8;
    text-align: center;
    color: white;
    position: relative;
    /* Memberikan efek bayangan (glow) biru keren! */
    box-shadow: 0 10px 25px rgba(56, 189, 248, 0.3);
}

/* 4. Lencana Level */
.lencana-level {
    background-color: #f59e0b;
    color: black;
    font-weight: bold;
    padding: 4px 12px;
    border-radius: 12px;
    display: inline-block;
    font-size: 12px;
    margin-bottom: 15px;
}

/* 5. Foto Profil Karakter (Membuat lingkaran dengan Border) */
.foto-karakter {
    width: 110px;
    height: 110px;
    background-color: #0f172a;
    border-radius: 50%;
    border: 3px solid #38bdf8;
    padding: 5px;
    margin: 0 auto 15px auto;
    display: block;
}

/* 6. Mengatur Gaya Teks Nama & Tipe */
.nama-karakter {
    font-size: 24px;
    color: #f8fafc;
    margin-bottom: 5px;
}

.tipe-karakter {
    font-size: 14px;
    color: #94a3b8;
    margin-bottom: 20px;
}

/* 7. Flexbox untuk Menyusun Statistik 3 Kolom Secara Sejajar */
.wadah-stats {
    display: flex;
    justify-content: space-between;
    background-color: #0f172a;
    padding: 12px;
    border-radius: 12px;
    margin-bottom: 20px;
}

.stat-box {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.angka-stat {
    font-weight: bold;
    font-size: 15px;
    color: #38bdf8;
}

.label-stat {
    font-size: 11px;
    color: #64748b;
    margin-top: 2px;
}

/* 8. Tombol Main dengan Efek Hover Keren */
.tombol-main {
    width: 100%;
    padding: 12px;
    background-color: #38bdf8;
    color: #0f172a;
    border: none;
    border-radius: 10px;
    font-size: 16px;
    font-weight: bold;
    cursor: pointer;
    transition: 0.3s;
}

/* Efek saat tombol di-sentuh kursor mouse! */
.tombol-main:hover {
    background-color: #f59e0b;
    color: black;
}
```

---

## 🎯 Rangkuman Kilat (Cheat Sheet untuk Anak-Anak) 🧠

| Konsep CSS | Kunci Rahasia / Analogi | Contoh Kode |
| :--- | :--- | :--- |
| **Selector** | Memilih elemen mana yang dihias (`.class`, `#id`, `tag`) | `.tombol { }` |
| **Color** | Mewarnai teks & latar belakang | `color: red; background-color: blue;` |
| **Font** | Mengubah ukuran, gaya, & jenis tulisan | `font-size: 20px; font-family: Arial;` |
| **Margin** | Jarak **LUAR** elemen ke elemen tetangga | `margin: 20px;` |
| **Padding** | Jarak **DALAM** elemen dari isi ke pinggir | `padding: 15px;` |
| **Border** | Pagar / bingkai elemen (Tebal, Gaya, Warna) | `border: 2px solid black;` |
| **Border-Radius** | Sudut bulat melengkung / lingkaran | `border-radius: 10px;` (atau `50%`) |
| **Display** | Cara elemen tampil (`block`, `inline`, `inline-block`) | `display: inline-block;` |
| **Flexbox** | Kotak ajaib penyusun tata letak serba rapi | `display: flex; justify-content: center;` |

---

Selamat! Kamu sudah menguasai fondasi dasar **CSS**! Sekarang giliranmu mencoba mengubah warna, ukuran, dan bentuk kartu karakter game di atas sesuai imajinasimu! 🚀🎨
