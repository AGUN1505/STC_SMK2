# 🌐 Pertemuan 1: Pengenalan Pemrograman Web & Persiapan Alat Tempur! 🚀

Selamat datang di modul **Pertemuan 1**! Di sini kita akan memulai petualangan seru belajar dunia **Pemrograman Web**. 

Sebelum kita mahir membuat web keren seperti YouTube, Roblox, atau Instagram, kita wajib paham dulu bagaimana cara kerja dunia web di balik layar dan menyiapkan **alat tempur** (software) yang akan kita gunakan sehari-hari!

---

## 📚 Daftar Isi
1. 🌐 [Apa itu Internet & Web?](#1-apa-itu-internet--web)
2. 🍔 [Konsep Client-Server (Analogi Restoran)](#2-konsep-client-server)
3. 💬 [Memahami HTTP & HTTPS](#3-memahami-http--https)
4. 🌐 [Web Browser: Pelayan Halaman Web](#4-web-browser)
5. 🏢 [Web Server: Koki Penyedia Web](#5-web-server)
6. 🛠️ [Instalasi Laragon / XAMPP (Server Lokal di Laptop)](#6-instalasi-laragon--xampp)
7. 💻 [Instalasi & Setup VS Code (Code Editor Pahlawan)](#7-instalasi--setup-vs-code)
8. 🧪 [Praktik Pertama: Proyek "Hello World!"](#8-praktik-pertama-proyek-hello-world)
9. 🎯 [Rangkuman & Kuis Asyik](#9-rangkuman--kuis-asyik)

---

<a name="1-apa-itu-internet--web"></a>
## 1. 🌐 Apa itu Internet & Web?

Banyak orang mengira **Internet** dan **Web** adalah hal yang sama. Padahal mereka adalah dua hal yang berbeda tapi saling bekerjasama!

💡 **Analogi Sederhana:**
* **Internet** = **Jalan Raya Raksasa dan Kabel-Kabel** yang menghubungkan seluruh komputer di dunia.
* **Web (World Wide Web / WWW)** = **Mobil, Bus, dan Pertokoan** yang berjalan di atas jalan raya internet tersebut. Web adalah tempat kita membaca informasi, menonton video, dan bermain game secara visual.

> 🌟 **Fakta Unik:** Tanpa Internet, komputer kamu tidak punya jalan untuk menyapa komputer di Amerika atau Jepang. Tanpa Web, jalan raya internet akan sepi karena tidak ada website untuk dikunjungi!

---

<a name="2-konsep-client-server"></a>
## 2. 🍔 Konsep Client-Server (Analogi Restoran)

Bagaimana bisa saat kamu mengetik `www.google.com` di HP-mu, gambar dan teks Google langsung muncul dalam sekejap? Itu terjadi karena ada kerjasama antara **Client** dan **Server**.

💡 **Analogi Restoran Burger:**

```text
+---------------------+               +---------------------+
|       CLIENT        |               |       SERVER        |
|  (Kamu & HP/Komputer)|               |   (Komputer Pusat)  |
|                     |   1. Pesan    |                     |
|    [  Pelanggan  ]  |-------------->|    [  Koki Dapur ]  |
|                     |  (Request)    |                     |
|                     |<--------------|                     |
|                     |  2. Makanan   |                     |
|                     |  (Response)   |                     |
+---------------------+               +---------------------+
```

1. **Client (Pelanggan / Pembeli):**
   * Ini adalah **laptop, HP, atau tablet** yang kamu gunakan saat menjelajah internet.
   * Client bertugas **meminta (Request)** informasi. Seperti kamu yang datang ke restoran dan berkata: *"Mbak, saya mau pesan 1 Burger Sapi!"*

2. **Server (Koki & Dapur Restoran):**
   * Ini adalah **komputer raksasa yang super cepat** milik Google, YouTube, atau Roblox yang hidup 24 jam nonstop tanpa pernah dimatikan.
   * Server bertugas **meracik dan mengirimkan (Response)** data yang diminta client. Koki di dapur akan memasak burger, lalu mengirimkannya kembali ke meja pembeli.

---

<a name="3-memahami-http--https"></a>
## 3. 💬 Memahami HTTP & HTTPS

Saat Pelanggan (*Client*) berbicara dengan Koki (*Server*), mereka harus memakai bahasa dan aturan yang sama. Aturan komunikasi ini disebut **HTTP**.

**HTTP** singkatan dari *HyperText Transfer Protocol*.

```text
CLIENT ------------------- [ HTTP Request ] -------------------> SERVER
"Tolong kirim file index.html!"

CLIENT <------------------- [ HTTP Response ] ------------------ SERVER
"Ini filenya! (Status: 200 OK)"
```

### 📩 Kode Status HTTP yang Populer:
Saat Server merespons Client, Server selalu menyertakan kode rahasia:
* **200 OK:** *"Pesananmu berhasil dibuat dan dikirim!"* (Web muncul dengan lancar).
* **404 Not Found:** *"Maaf, halaman yang kamu cari tidak ada di dapur kami!"* 😢
* **500 Internal Server Error:** *"Koki di dapur lagi pusing / kompornya error!"* (Server sedang bermasalah).

---

### 🔒 Bedanya HTTP vs HTTPS:
Pernahkah kamu melihat ikon **Gembok** di sebelah alamat web?

* **HTTP (Tanpa Gembok):** Seperti mengirim surat tanpa amplop. Siapa saja di jalanan bisa mengintip isi pesanmu (password, nomor HP).
* **HTTPS (Dengan Gembok / *Secure*):** Seperti mengirim surat di dalam **brankas terkunci rahasia**. Datamu diacak (dienkripsi) sehingga aman dari peretas (*hacker*)!

---

<a name="4-web-browser"></a>
## 4. 🌐 Web Browser: Pelayan Halaman Web

**Web Browser** adalah aplikasi yang ada di komputer/HP kamu yang bertugas menjadi "Pelayan" antara kamu dan Server.

### Tugas Utama Browser:
1. Meminta file HTML, CSS, dan JavaScript dari Server di seluruh dunia.
2. Menerjemahkan bahasa kode yang rumit menjadi tampilan gambar, warna, dan tombol yang cantik di layarmu.

### 🦊 Contoh Web Browser Populer:
* **Google Chrome** (Paling populer & cepat)
* **Mozilla Firefox**
* **Microsoft Edge**
* **Safari** (Untuk pengguna Apple)

---

<a name="5-web-server"></a>
## 5. 🏢 Web Server: Koki Penyedia Web

**Web Server** adalah program yang berjalan di komputer server untuk menyimpan file-file website (HTML, CSS, JS, Gambar, Database) dan membagikannya ke orang-orang yang mengaksesnya.

### 🌟 Contoh Aplikasi Web Server:
* **Apache** (Sangat populer dan stabil)
* **Nginx** (Super cepat untuk website raksasa)
* **LiteSpeed**

### 🏠 Localhost (Server Lokal):
Sebelum website kita diunggah ke internet agar bisa dilihat semua orang di dunia, kita biasanya mencobanya dulu di komputer sendiri. Komputer kita disulap menjadi server buatan yang dinamakan **Localhost**!

---

<a name="6-instalasi-laragon--xampp"></a>
## 6. 🛠️ Instalasi Laragon / XAMPP (Server Lokal di Laptop)

Untuk menyulap laptop kamu menjadi Web Server lokal, kita membutuhkan aplikasi penyedia server buatan. Ada dua aplikasi populer: **Laragon** (Sangat direkomendasikan untuk pemula karena cepat dan ringan) atau **XAMPP**.

---

### 🚀 Opsi A: Instalasi Laragon (Rekomendasi Utama)

**Laragon** adalah aplikasi server lokal modern untuk Windows yang sangat mudah digunakan, super cepat, dan tidak bikin laptop lemot.

#### Langkah-Langkah Instalasi Laragon:
1. **Download Laragon:**
   * Buka browser dan kunjungi: [https://laragon.org/download/](https://laragon.org/download/)
   * Pilih **Laragon Full** (termasuk Apache, MySQL, PHP).

2. **Jalankan Installer:**
   * Buka file installer yang sudah didownload (contoh: `laragon-wamp.exe`).
   * Pilih bahasa: **English** ➡️ Klik **Next**.
   * Pilih lokasi instalasi (Default: `C:\laragon`) ➡️ Klik **Next**.

3. **Pengaturan Awal:**
   * Centang *"Run Laragon when Windows starts"* (Opsional) dan *"Auto virtual hosts"* (Centang ini agar sangat memudahkan).
   * Klik **Next** ➡️ Klik **Install**.
   * Tunggu hingga proses instalasi selesai, lalu klik **Finish**.

4. **Cara Menjalankan Laragon:**
   * Buka aplikasi Laragon di laptopmu.
   * Klik tombol **Start All** yang berwarna hijau besar!
   * Jika muncul jendela konfirmasi Windows Firewall, klik **Allow Access**.
   * Buka browser, lalu ketik `http://localhost`. Jika muncul halaman ucapan selamat dari Laragon, artinya **Server Lokalmu Sudah Berhasil Aktif!** 🎉

```text
[ Tampilan Utama Laragon ]
+------------------------------------------+
|  Laragon Full                             |
|                                          |
|   [  START ALL  ]   [ Web ]  [ Database ]|
|                                          |
|  Apache 2.4  |  MySQL 8.0  |  PHP 8.1    |
+------------------------------------------+
```

---

### 📦 Opsi B: Instalasi XAMPP (Alternatif)

Jika laptopmu sudah terpasang **XAMPP**, kamu juga bisa menggunakannya!

#### Langkah-Langkah Singkat XAMPP:
1. Download XAMPP dari [apachefriends.org](https://www.apachefriends.org/).
2. Jalankan installer dan ikuti petunjuk tekan **Next** sampai selesai.
3. Buka **XAMPP Control Panel**.
4. Klik tombol **Start** pada modul **Apache** dan **MySQL** hingga indikatornya berwarna hijau.
5. Buka browser dan ketik `http://localhost`.

---

<a name="7-instalasi--setup-vs-code"></a>
## 7. 💻 Instalasi & Setup VS Code (Code Editor Pahlawan)

Sebagai calon *Developer Web*, kita butuh tempat menulis kode yang nyaman. **Visual Studio Code (VS Code)** adalah aplikasi editor kode gratis buatan Microsoft yang paling banyak digunakan di seluruh dunia!

---

### 📥 Langkah Instalasi VS Code:
1. Kunjungi situs resmi: [https://code.visualstudio.com/](https://code.visualstudio.com/)
2. Klik tombol **Download for Windows**.
3. Buka file hasil download, centang *"I accept the agreement"* ➡️ Klik **Next**.
4. ⚠️ **PENTING:** Pada pilihan checkbox, centang semua opsi terutama:
   * ✅ *Add "Open with Code" to Windows Explorer file context menu*
   * ✅ *Add "Open with Code" to Windows Explorer directory context menu*
5. Klik **Next** ➡️ **Install** ➡️ **Finish**.

---

### 🧩 Extension Wajib untuk VS Code Pemula:
VS Code punya toko jurus/fitur tambahan bernama **Extensions**. Caranya tekan tombol `Ctrl + Shift + X` di dalam VS Code, lalu cari nama extension di bawah ini dan klik **Install**:

1. ⚡ **Live Server** *(by Ritwick Dey)*:
   * **Fungsinya:** Menjalankan web lokal secara otomatis. Begitu kamu simpan kode (`Ctrl + S`), tampilan web di browser langsung berubah tanpa perlu di-refresh manual!
2. 🎨 **Material Icon Theme** *(by Philipp Kief)*:
   * **Fungsinya:** Mengubah ikon folder dan file di VS Code menjadi sangat cantik dan mudah dikenali.
3. 🧹 **Prettier - Code Formatter**:
   * **Fungsinya:** Merapikan baris-baris kode yang berantakan secara otomatis.
4. 🏷️ **Auto Rename Tag**:
   * **Fungsinya:** Saat kamu mengubah nama tag pembuka HTML (misal `<h1` jadi `<h2`), tag penutupnya `</h1>` akan ikut berubah otomatis!

---

<a name="8-praktik-pertama-proyek-hello-world"></a>
## 8. 🧪 Praktik Pertama: Proyek "Hello World!"

Saatnya kita mencoba membuat website pertama kita di laptop sendiri!

### Langkah 1: Buat Folder Project Baru
* Buka File Explorer laptopmu.
* Jika menggunakan **Laragon**, masuk ke folder: `C:\laragon\www\`
* Buat folder baru bernama: `web-pertamaku`

### Langkah 2: Buka Folder di VS Code
* Buka aplikasi **VS Code**.
* Klik menu **File ➡️ Open Folder...**
* Pilih folder `C:\laragon\www\web-pertamaku`, lalu klik **Select Folder**.

### Langkah 3: Buat File `index.html`
* Di sebelah kiri VS Code, klik ikon **New File** (kertas dengan tanda plus).
* Beri nama file: `index.html`

### Langkah 4: Tulis Kode HTML Pertama
Ketik kode sederhana di bawah ini ke dalam file `index.html`:

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Website Pertamaku</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #e0f2fe;
            text-align: center;
            padding-top: 50px;
        }
        h1 {
            color: #0284c7;
        }
        p {
            color: #334155;
            font-size: 18px;
        }
        .kotak-sukses {
            background-color: white;
            display: inline-block;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body>

    <div class="kotak-sukses">
        <h1>🎉 Hello World!</h1>
        <p>Selamat! Saya berhasil membuat halaman web pertama di laptop sendiri!</p>
        <p><i>- Calon Web Developer Hebat 🚀</i></p>
    </div>

</body>
</html>
```

### Langkah 5: Jalankan di Browser!
1. Simpan file dengan menekan **`Ctrl + S`**.
2. **Cara 1 (Menggunakan Live Server):** Klik kanan di dalam area kode `index.html` di VS Code, lalu pilih **"Open with Live Server"**.
3. **Cara 2 (Lewat Laragon):** Buka browser dan ketik alamat: `http://localhost/web-pertamaku`

Hore! Halaman web pertama buatanmu sendiri berhasil tampil anggun di layar! 🥳✨

---

<a name="9-rangkuman--kuis-asyik"></a>
## 9. 🎯 Rangkuman & Kuis Asyik

### 🧠 Rangkuman Ringkas:
* **Client** = Laptop/HP kamu yang meminta halaman web.
* **Server** = Komputer pusat 24 jam yang menyimpan file website dan meracik balasan.
* **HTTP/HTTPS** = Bahasa / Aturan percakapan antara Client dan Server (HTTPS lebih aman karena ber-gembok).
* **Laragon / XAMPP** = Aplikasi untuk menyulap laptop pribadi jadi Server Lokal (*Localhost*).
* **VS Code** = Aplikasi editor kode terbaik tempat kita mengetik perintah HTML, CSS, dan JS.

---

### 🧩 Kuis Detektif Web! 🕵️‍♂️

Cobalah jawab 4 pertanyaan seru ini untuk menguji pemahamanmu:

1. Kalau di restoran burger, siapakah yang bertindak sebagai **Server**?
   * a) Pelanggan yang duduk di meja
   * b) Koki yang memasak di dapur
   * c) Buku menu makanan

2. Apa arti dari kode angka rahasia **404 Not Found** saat kamu membuka web?
   * a) Web berhasil dibuka dengan sukses
   * b) Komputer kamu mati
   * c) Halaman web yang dicari tidak ditemukan di server

3. Di manakah lokasi folder utama untuk menaruh proyek web jika menggunakan aplikasi Laragon?
   * a) `C:\Windows\`
   * b) `C:\laragon\www\`
   * c) `C:\Program Files\`

4. Extension VS Code apa yang membuat tampilan web di browser otomatis berubah begitu kita menekan `Ctrl + S`?
   * a) Live Server
   * b) Auto Rename Tag
   * c) Calculator

---

*Jawaban Kuis: 1. (b), 2. (c), 3. (b), 4. (a)*

**Selamat! Kamu sudah menyelesaikan Pertemuan 1 dengan sangat luar biasa! Sampai jumpa di Pertemuan 2! 🚀**
