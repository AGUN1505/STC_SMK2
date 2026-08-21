# 🦴 Pertemuan 2: Menguasai HTML Dasar - Membangun Kerangka Website! 🏗️

Selamat datang di **Pertemuan 2**! Jika di Pertemuan 1 kita sudah mengenal konsep web dan menyiapkan alat tempurnya (VS Code & Laragon), di pertemuan ini kita akan mulai **menulis kode web pertama kita menggunakan HTML!**

---

## 📚 Daftar Isi
1. 🏗️ [Apa itu HTML & Anatomi Tag](#1-apa-itu-html--anatomi-tag)
2. 🦴 [Struktur Utama HTML5 (Kerangka Dasar)](#2-struktur-utama-html5)
3. 🏷️ [Heading: Menulis Judul Halaman (h1 - h6)](#3-heading-menulis-judul-halaman)
4. 📝 [Paragraph & Format Teks (p, br, b, i, u)](#4-paragraph--format-teks)
5. 📋 [List: Membuat Daftar Rapi (ol, ul, li)](#5-list-membuat-daftar-rapi)
6. 🔗 [Link: Pintu Ajaib Berpindah Halaman (<a>)](#6-link-pintu-ajaib-berpindah-halaman)
7. 🖼️ [Image: Memasang Gambar di Web (<img>)](#7-image-memasang-gambar-di-web)
8. 📊 [Table: Menyusun Data Rapi Berbentuk Tabel](#8-table-menyusun-data-rapi-berbentuk-tabel)
9. 🎮 [Project Seru: Web "Biodata Pahlawan Digital"](#9-project-seru-web-biodata-pahlawan-digital)
10. 🎯 [Rangkuman & Kuis Detektif HTML](#10-rangkuman--kuis-detektif-html)

---

<a name="1-apa-itu-html--anatomi-tag"></a>
## 1. 🏗️ Apa itu HTML & Anatomi Tag

**HTML** singkatan dari *HyperText Markup Language*. 

💡 **Analogi Sederhana:**
* **HTML** itu seperti **Tulang dan Kerangka Tubuh Manusia** atau **Struktur Bangunan Rumah**.
* Tanpa kerangka tulang, manusia tidak bisa berdiri tegap. Tanpa HTML, website tidak punya bentuk!

---

### 🔬 Anatomi Tag HTML (Cara Membaca Kode HTML)
Hampir semua elemen di HTML ditulis menggunakan sepasang **Tag**:

```text
  Tag Pembuka             Isi / Konten             Tag Penutup
   (Opening)                                        (Closing)
  +--------+                                       +---------+
  |  <p>   |  Halo, saya sedang belajar HTML!     |  </p>   |
  +--------+                                       +---------+
```

* **Tag Pembuka:** `<nama_tag>` (Diawali tanda `<` dan diakhiri `>`).
* **Konten:** Teks atau gambar yang ada di tengah-tengahnya.
* **Tag Penutup:** `</nama_tag>` (Sama seperti tag pembuka, tapi ada tanda garis miring `/`).

---

<a name="2-struktur-utama-html5"></a>
## 2. 🦴 Struktur Utama HTML5 (Kerangka Dasar)

Setiap file HTML **wajib** memiliki 4 struktur utama ini. Bayangkan seperti struktur tubuh manusia:

```text
+-------------------------------------------------------+
|  <!DOCTYPE html>  --> (Surat Izin HTML5)              |
|  <html lang="id"> --> (Seluruh Tubuh Manusia)         |
|                                                       |
|    <head>         --> (Kepala / Otak)                 |
|      <title>Judul Tab Browser</title>                 |
|    </head>                                            |
|                                                       |
|    <body>         --> (Badan / Semua yang Terlihat)   |
|      <h1>Judul Utama</h1>                             |
|      <p>Isi teks halaman web...</p>                   |
|    </body>                                            |
|                                                       |
|  </html>                                              |
+-------------------------------------------------------+
```

### Kode Kerangka Standar HTML5:

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Halaman Web Pertama Saya</title>
</head>
<body>

    <!-- Semua isi website yang terlihat oleh pengunjung ditulis di sini! -->
    <h1>Selamat Datang di Web Saya!</h1>

</body>
</html>
```

### 🔍 Penjelasan Komponen:
1. `<!DOCTYPE html>` = Memberitahu browser: *"Hei Browser, dokumen ini memakai standar HTML5 terbaru!"*
2. `<html lang="id">` = Wadah utama seluruh kode web (Bahasa yang digunakan adalah Bahasa Indonesia).
3. `<head>` = Kepala dokumen. Berisi informasi rahasia untuk browser (seperti judul tab, ikon, dan kata kunci), isi di dalam `<head>` **tidak akan muncul** di area halaman web.
4. `<body>` = Badan dokumen. Semua teks, gambar, tombol, dan video yang **terlihat di layar** wajib ditulis di dalam `<body>`.

> ⚡ **Jurus Rahasia VS Code (Emmet):**
> Kamu tidak perlu mengetik kerangka di atas secara manual! Cukup buka file `.html` kosong di VS Code, ketik tanda seru **`!`** lalu tekan tombol **`Enter`** atau **`Tab`**. Kerangka HTML5 akan langsung muncul otomatis! Magic! 🪄

---

<a name="3-heading-menulis-judul-halaman"></a>
## 3. 🏷️ Heading: Menulis Judul Halaman (h1 - h6)

**Heading** digunakan untuk membuat judul atau sub-judul di halaman web. Di HTML ada 6 tingkat heading, dari yang terbesar `<h1>` sampai yang terkecil `<h6>`.

```html
<h1>Heading 1 (Judul Utama Paling Besar)</h1>
<h2>Heading 2 (Sub Judul Bab)</h2>
<h3>Heading 3 (Sub-sub Judul)</h3>
<h4>Heading 4 (Judul Kecil)</h4>
<h5>Heading 5 (Judul Lebih Kecil)</h5>
<h6>Heading 6 (Judul Paling Kecil)</h6>
```

### 📊 Ukuran Visual Heading:
* `<h1>`: Ukuran sangat besar dan tebal.
* `<h2>` s/d `<h3>`: Ukuran sedang untuk membagi bab/topik.
* `<h4>` s/d `<h6>`: Ukuran kecil.

⚠️ **Aturan Emas SEO & Desain:**
Dalam **1 halaman web**, sangat disarankan hanya ada **SATU `<h1>`** (Judul Utama). Gunakan `<h2>` atau `<h3>` untuk bagian-bagian di bawahnya.

---

<a name="4-paragraph--format-teks"></a>
## 4. 📝 Paragraph & Format Teks (p, br, b, i, u)

### A. Tag Paragraf `<p>`
Untuk menulis tulisan cerita, artikel, atau deskripsi, gunakan tag `<p>`. Browser akan otomatis memberikan jarak spasi atas dan bawah untuk tiap paragraf.

```html
<p>Ini adalah paragraf pertama saya di web. Tulisannya akan rapi dan otomatis membaris sendiri.</p>
<p>Ini adalah paragraf kedua. Berada tepat di bawah paragraf pertama.</p>
```

---

### B. Tag Ganti Baris `<br>` dan Garis Pemisah `<hr>`
* `<br>` *(Break)* = Memaksa teks pindah ke baris baru **tanpa** membuat paragraf baru.
* `<hr>` *(Horizontal Rule)* = Membuat garis lurus pembatas secara horizontal dari kiri ke kanan.

> 💡 *Catatan:* Tag `<br>` dan `<hr>` adalah **Self-Closing Tag** (tidak butuh tag penutup `</br>`).

```html
<p>Alamat Rumah Saya:<br>
Jl. Merdeka No. 45<br>
Jakarta Selatan</p>

<hr> <!-- Garis pembatas horizontal -->
```

---

### C. Tag Menghias Teks (Formatting Text):
* `<b>` atau `<strong>` = Membuat teks **Tebal / Bold**.
* `<i>` atau `<em>` = Membuat teks *Miring / Italic*.
* `<u>` = Membuat teks <u>Garis Bawah / Underline</u>.
* `<mark>` = Membuat efek <mark>Stabilo Kuning</mark>.

```html
<p>Saya belajar <b>HTML Dasar</b> dengan rasa <i>semangat</i> yang <u>tinggi</u> dan <mark>gembira</mark>!</p>
```

---

<a name="5-list-membuat-daftar-rapi"></a>
## 5. 📋 List: Membuat Daftar Rapi (ol, ul, li)

Saat kamu ingin membuat daftar belanjaan, langkah-langkah resep, atau daftar hobi, gunakan tag **List**.

Setiap item di dalam daftar **wajib** dibungkus dengan tag `<li>` *(List Item)*.

---

### A. Unordered List `<ul>` (Daftar Poin / Simbol Bulat)
Digunakan jika urutan daftar **tidak berpengaruh** (bebas).

```html
<h3>🛒 Daftar Belanjaan:</h3>
<ul>
    <li>Buah Apel</li>
    <li>Susu Sapi</li>
    <li>Roti Tawar</li>
</ul>
```
**Hasil di Layar:**
* Buah Apel
* Susu Sapi
* Roti Tawar

---

### B. Ordered List `<ol>` (Daftar Berurutan Angka / Huruf)
Digunakan jika urutan **sangat penting** (seperti langkah-langkah / peringkat).

```html
<h3>🏆 Juara Lomba Lari:</h3>
<ol>
    <li>Budi Santoso</li>
    <li>Siti Aminah</li>
    <li>Doni Pratama</li>
</ol>
```
**Hasil di Layar:**
1. Budi Santoso
2. Siti Aminah
3. Doni Pratama

---

<a name="6-link-pintu-ajaib-berpindah-halaman"></a>
## 6. 🔗 Link: Pintu Ajaib Berpindah Halaman (`<a>`)

**Link** (Pranala) adalah fitur paling ajaib di web yang memungkinkan kita berpindah dari satu halaman ke halaman lain hanya dengan sekali klik!

Di HTML, link dibuat menggunakan tag `<a>` *(Anchor)* dengan atribut wajib `href="..."` *(Hypertext Reference)*.

```html
<!-- Link menuju website luar -->
<a href="https://www.google.com">Buka Google</a>

<!-- Link menuju halaman lain di laptop sendiri -->
<a href="tentang.html">Buka Halaman Tentang Saya</a>
```

### 🚀 Trik Membuka Link di Tab Baru:
Gunakan atribut `target="_blank"` agar saat link diklik, browser membuka halaman tersebut di **tab baru** tanpa menutup halamanmu!

```html
<a href="https://www.youtube.com" target="_blank">Nonton YouTube di Tab Baru</a>
```

---

<a name="7-image-memasang-gambar-di-web"></a>
## 7. 🖼️ Image: Memasang Gambar di Web (`<img>`)

Halaman web tanpa gambar tentu terasa sepi. Untuk menampilkan gambar, kita gunakan tag `<img>`.

 Tag `<img>` juga termasuk **Self-Closing Tag** (tidak punya tag penutup `</img>`).

```html
<img src="foto-hero.jpg" alt="Foto Robot Pahlawan" width="200">
```

### 🔬 Atribut Wajib Tag `<img>`:
1. `src="..."` *(Source)* = Alamat / lokasi file gambar (bisa nama file lokal atau URL internet).
2. `alt="..."` *(Alternative Text)* = Teks penjelasan jika gambar gagal dimuat (sangat penting untuk tuna netra & Google SEO).
3. `width="..."` & `height="..."` = Mengatur lebar dan tinggi gambar dalam piksel (`px`).

---

<a name="8-table-menyusun-data-rapi-berbentuk-tabel"></a>
## 8. 📊 Table: Menyusun Data Rapi Berbentuk Tabel

Tabel digunakan untuk menampilkan data berformat kolom dan baris (seperti Jadwal Pelajaran atau Daftar Nilai).

### 🧩 Elemen Penyusun Tabel:
* `<table>` = Wadah utama tabel.
* `<tr>` *(Table Row)* = Baris mendatar (Kiri ke Kanan).
* `<th>` *(Table Header)* = Judul kolom (Teks otomatis **tebal** dan di **tengah**).
* `<td>` *(Table Data)* = Isi sel data biasa.

```html
<table border="1">
    <!-- Baris 1: Judul Kolom -->
    <tr>
        <th>No</th>
        <th>Nama Pelajaran</th>
        <th>Hari</th>
    </tr>
    <!-- Baris 2: Data Ke-1 -->
    <tr>
        <td>1</td>
        <td>Pemrograman Web</td>
        <td>Senin</td>
    </tr>
    <!-- Baris 3: Data Ke-2 -->
    <tr>
        <td>2</td>
        <td>Basis Data</td>
        <td>Selasa</td>
    </tr>
</table>
```

### 📐 Menggabungkan Sel Tabel:
* `colspan="2"` = Menggabungkan beberapa **Kolom** ke samping.
* `rowspan="2"` = Menggabungkan beberapa **Baris** ke bawah.

```html
<!-- Contoh gabung 2 kolom -->
<td colspan="2">Libur Akhir Pekan</td>
```

---

<a name="9-project-seru-web-biodata-pahlawan-digital"></a>
## 9. 🎮 Project Seru: Web "Biodata Pahlawan Digital"

Yuk gabungkan **SEMUA elemen HTML** yang sudah kita pelajari hari ini untuk membuat website **Biodata Diri Pahlawan Digital**!

### 📝 Salin Kode HTML Ini ke File `index.html`:

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Biodata Pahlawan Digital</title>
</head>
<body style="font-family: Arial, sans-serif; line-height: 1.6; padding: 20px; background-color: #f4f7fe;">

    <!-- 1. Heading Utama -->
    <h1>🚀 Profil Pahlawan Digital</h1>
    <p><i>"Belajar coding hari ini untuk mengubah dunia esok hari!"</i></p>
    <hr>

    <!-- 2. Foto & Deskripsi Singkat -->
    <h2>👤 Tentang Saya</h2>
    <img src="https://api.dicebear.com/7.x/bottts/svg?seed=PahlawanWeb" alt="Foto Avatar Saya" width="150">
    
    <p>Halo semuanya! Nama saya <b>Alex Budi</b>. Saya adalah seorang siswa yang bercita-cita menjadi <mark>Full-Stack Web Developer</mark> yang hebat. Saya suka memecahkan masalah dan membuat aplikasi web yang bermanfaat.</p>

    <!-- 3. Unordered List & Ordered List -->
    <h2>🎯 Keahlian & Hobi</h2>
    
    <h3>Hobi Favorit:</h3>
    <ul>
        <li>Belajar Kode HTML & CSS</li>
        <li>Bermain Game Puzzle & Strategi</li>
        <li>Membaca Buku Teknologi</li>
    </ul>

    <h3>Target Belajar Minggu Ini:</h3>
    <ol>
        <li>Menguasai Tag Dasar HTML5</li>
        <li>Membuat Tabel & List yang Rapi</li>
        <li>Menghubungkan Web dengan Link Keren</li>
    </ol>

    <!-- 4. Tabel Jadwal Belajar -->
    <h2>📅 Jadwal Belajar Coding Mingguan</h2>
    <table border="1" cellpadding="8" cellspacing="0" style="background-color: white;">
        <tr style="background-color: #0284c7; color: white;">
            <th>Hari</th>
            <th>Materi Belajar</th>
            <th>Durasi</th>
        </tr>
        <tr>
            <td>Senin</td>
            <td>Struktur & Tag HTML5</td>
            <td>2 Jam</td>
        </tr>
        <tr>
            <td>Rabu</td>
            <td>Membuat Tabel & Form</td>
            <td>2 Jam</td>
        </tr>
        <tr>
            <td>Jumat</td>
            <td>Mewarnai Web dengan CSS</td>
            <td>3 Jam</td>
        </tr>
    </table>

    <br>
    <hr>

    <!-- 5. Link Kontak -->
    <h2>📬 Hubungi Saya</h2>
    <p>Ingin berdiskusi atau belajar bareng? Silakan kunjungi link di bawah ini:</p>
    <p>
        👉 <a href="https://github.com" target="_blank">Kunjungi Profil GitHub Saya</a> | 
        👉 <a href="https://google.com" target="_blank">Cari Saya di Google</a>
    </p>

</body>
</html>
```

---

<a name="10-rangkuman--kuis-detektif-html"></a>
## 10. 🎯 Rangkuman & Kuis Detektif HTML

### 🧠 Cheat Sheet Tag HTML Dasar:

| Nama Tag | Fungsi Utama | Contoh Penulisan |
| :--- | :--- | :--- |
| `<!DOCTYPE html>` | Menandai dokumen standar HTML5 | `<!DOCTYPE html>` |
| `<html>` | Wadah utama akar seluruh kode | `<html lang="id">...</html>` |
| `<head>` | Kepala dokumen (Informasi rahasia browser) | `<title>Judul Web</title>` |
| `<body>` | Badan dokumen (Konten terlihat di layar) | `<body>...</body>` |
| `<h1>` - `<h6>` | Judul / Heading (Terbesar ke Terkecil) | `<h1>Judul Utama</h1>` |
| `<p>` | Paragraf teks | `<p>Ini paragraf...</p>` |
| `<br>` | Ganti baris baru (Self-Closing) | `Teks1 <br> Teks2` |
| `<ul>` & `<li>` | Daftar poin / simbol | `<ul><li>Item</li></ul>` |
| `<ol>` & `<li>` | Daftar berurutan angka (1, 2, 3) | `<ol><li>Item</li></ol>` |
| `<a>` | Link pintu ajaib berpindah halaman | `<a href="https://...">Klik</a>` |
| `<img>` | Memasang gambar (Self-Closing) | `<img src="a.jpg" alt="Foto">` |
| `<table>` | Wadah pembuat tabel rapi | `<table><tr><td>...</td></tr></table>` |

---

### 🧩 Kuis Detektif HTML 🕵️‍♀️

Jawab 4 pertanyaan kilat ini untuk membuktikan kamu sudah jadi Ahli HTML:

1. Di dalam bagian manakah semua teks, gambar, dan tombol yang **terlihat oleh pengunjung web** ditulis?
   * a) `<head>`
   * b) `<body>`
   * c) `<!-- comment -->`

2. Manakah tag yang benar untuk membuat teks menjadi **tebal**?
   * a) `<i>`
   * b) `<u>`
   * c) `<b>` atau `<strong>`

3. Atribut wajib apa yang digunakan pada tag `<img>` untuk memberi tahu alamat lokasi file gambar?
   * a) `href`
   * b) `src`
   * c) `target`

4. Apa fungsi dari atribut `target="_blank"` saat dipasang pada tag link `<a>`?
   * a) Membuka halaman link di tab browser yang baru
   * b) Menghapus link secara permanen
   * c) Mengubah warna link jadi hitam

---

*Kunci Jawaban Kuis: 1. (b), 2. (c), 3. (b), 4. (a)*

**Luar Biasa! Kamu berhasil menyelesaikan Pertemuan 2 tentang HTML Dasar dengan nilai sempurna! Sampai jumpa di Pertemuan 3! 🚀✨**
