# 📝 Pertemuan 3: Menguasai HTML Form - Membuat Formulir Interaktif & Validasi! 🚀

Selamat datang di **Pertemuan 3**! Di dua pertemuan sebelumnya, kita sudah belajar cara kerja web dan menyusun kerangka dokumen (teks, gambar, tabel). Sekarang saatnya membuat website kita **bisa berinteraksi dan menerima masukan dari pengunjung** dengan menggunakan **HTML Form**!

---

## 📚 Daftar Isi
1. 📝 [Apa itu HTML Form? (Analogi Formulir Pendaftaran)](#1-apa-itu-html-form)
2. 📦 [Elemen Utama `<form>` & Atribut Action/Method](#2-elemen-utama-form)
3. 🔤 [Elemen Input & Jenis-Jenisnya (Text, Password, Email, Radio, Checkbox, dll)](#3-elemen-input--jenis-jenisnya)
4. 🏷️ [Pentingnya Tag `<label>` untuk Kenyamanan Pengguna](#4-pentingnya-tag-label)
5. 🔽 [Select & Option: Menu Pilihan Dropdown](#5-select--option-menu-pilihan-dropdown)
6. 📄 [Textarea: Kotak Pesan Panjang](#6-textarea-kotak-pesan-panjang)
7. 🔘 [Button: Tombol Kirim & Batal](#7-button-tombol-kirim--batal)
8. 🛡️ [Validasi HTML5: Satpam Penjaga Form (Required, Min, Max, dll)](#8-validasi-html5)
9. 🎮 [Project Seru: Mini Form Pendaftaran Akademi Gamer & Coding](#9-project-seru-mini-form-pendaftaran)
10. 🎯 [Rangkuman & Kuis Detektif Form](#10-rangkuman--kuis-detektif-form)

---

<a name="1-apa-itu-html-form"></a>
## 1. 📝 Apa itu HTML Form? (Analogi Formulir Pendaftaran)

Pernahkah kamu mendaftar akun Roblox, mengisi formulir pendaftaran ekskul di sekolah, atau mengetik kata di kolom pencarian Google? Semua itu dibuat menggunakan **HTML Form**!

💡 **Analogi Sederhana:**
* **HTML Form** itu seperti **Lembar Formulir Kertas** yang diberikan petugas pendaftaran.
* Kamu diminta mengisi nama di kotak nama, mencentang hobi, memilih tanggal lahir, dan menyerahkan kertas tersebut kembali ke petugas.

---

<a name="2-elemen-utama-form"></a>
## 2. 📦 Elemen Utama `<form>` & Atribut Action/Method

Semua komponen input harus dibungkus di dalam tag utama `<form>`.

```html
<form action="proses.php" method="POST">
    <!-- Komponen input ditulis di dalam sini! -->
</form>
```

### 🔬 Atribut Penting Tag `<form>`:
1. **`action="..."`** = Alamat tujuan ke mana data formulir ini akan dikirim (biasanya ke file pemroses di server seperti PHP atau Node.js).
2. **`method="..."`** = Cara pengiriman data:
   * **`GET`** (Terbuka): Data dimasukkan ke dalam URL browser. Cocok untuk **kolom pencarian** (Google/Search). ⚠️ *Tidak aman untuk password!*
   * **`POST`** (Rahasia): Data dibungkus rapat di dalam pesan rahasia (seperti amplop tertutup). Sangat aman untuk **login & pendaftaran password**!

---

<a name="3-elemen-input--jenis-jenisnya"></a>
## 3. 🔤 Elemen Input & Jenis-Jenisnya

Tag `<input>` adalah komponen paling serbaguna di HTML! Hanya dengan mengganti atribut `type="..."`, bentuk dan fungsinya bisa berubah drastis!

Tag `<input>` juga merupakan **Self-Closing Tag** (tidak butuh `</input>`).

```text
[ Input Text ]     : [ Budi Santoso               ]
[ Input Password ] : [ ••••••••••                 ]
[ Input Date ]     : [ 21 / 08 / 2026   📅       ]
[ Radio Button ]   : (•) Laki-laki   ( ) Perempuan
[ Checkbox ]       : [✓] Coding   [✓] Gaming   [ ] Musik
```

---

### 🎨 Tipe-Tipe Input Paling Populer:

#### 1. Input Teks Biasa (`type="text"`)
Untuk mengisi nama, username, atau alamat singkat.
```html
<input type="text" name="username">
```

#### 2. Input Kata Sandi (`type="password"`)
Teks yang diketik akan otomatis berubah menjadi titik-titik hitam (`•••`) agar tidak diintip orang di sebelahmu!
```html
<input type="password" name="password">
```

#### 3. Input Email (`type="email"`)
Otomatis memeriksa apakah pengguna mengetik format email yang benar (harus ada tanda `@` dan `.com`).
```html
<input type="email" name="user_email">
```

#### 4. Input Angka (`type="number"`)
Hanya bisa diisi angka (ada tombol panah naik-turun).
```html
<input type="number" name="umur">
```

#### 5. Input Tanggal (`type="date"`)
Muncul kalender pop-up otomatis untuk memilih tanggal lahir!
```html
<input type="date" name="tanggal_lahir">
```

#### 6. Radio Button (`type="radio"`)
Digunakan jika pengguna **HANYA BOLEH MEMILIH 1 PILIHAN** (misal: Jenis Kelamin).
* ⚠️ **PENTING:** Semua pilihan radio yang saling berhubungan wajib punya nama `name="..."` yang **sama persis**!

```html
<input type="radio" name="gender" value="L"> Laki-laki
<input type="radio" name="gender" value="P"> Perempuan
```

#### 7. Checkbox (`type="checkbox"`)
Digunakan jika pengguna **BOLEH MEMILIH LEBIH DARI 1 PILIHAN** (misal: Hobi / Minat).

```html
<input type="checkbox" name="hobi" value="coding"> Membaca Kode
<input type="checkbox" name="hobi" value="gaming"> Bermain Game
<input type="checkbox" name="hobi" value="musik"> Mendengar Musik
```

#### 8. Input Unggah File (`type="file"`)
Untuk mengunggah pas foto atau dokumen dari laptop.
```html
<input type="file" name="foto_profil">
```

#### 9. Input Pemilih Warna (`type="color"`)
Muncul kotak palet warna keren untuk memilih warna favorit!
```html
<input type="color" name="warna_favorit">
```

---

<a name="4-pentingnya-tag-label"></a>
## 4. 🏷️ Pentingnya Tag `<label>` untuk Kenyamanan Pengguna

Jangan langsung menaruh teks di sebelah kotak input! Selalu gunakan tag `<label>`.

💡 **Keunggulan Tag `<label>`:**
Jika pengguna mengklik **teks tulisan label-nya**, kursor akan **otomatis melompat aktif** masuk ke dalam kotak input terkait! Ini sangat memudahkan pengguna HP dengan jari besar.

### Cara Menghubungkan Label dan Input:
Gunakan atribut `for="..."` pada `<label>` dan id `id="..."` pada `<input>` dengan nilai yang **sama persis**.

```html
<label for="input-nama">Nama Lengkap:</label>
<input type="text" id="input-nama" name="nama_lengkap">
```

---

<a name="5-select--option-menu-pilihan-dropdown"></a>
## 5. 🔽 Select & Option: Menu Pilihan Dropdown

Jika opsi pilihan sangat banyak (misalnya daftar Kota atau Kelas), menggunakan Radio Button akan membuat halaman sangat panjang. Solusinya: Gunakan **Menu Dropdown** dengan `<select>` dan `<option>`!

```html
<label for="pilih-jurusan">Pilih Jurusan SMK:</label>
<select id="pilih-jurusan" name="jurusan">
    <option value="" disabled selected>-- Pilih Jurusan Kamu --</option>
    <option value="rpl">PPLG / Rekayasa Perangkat Lunak</option>
    <option value="tkj">TJKT / Teknik Jaringan</option>
    <option value="dkv">DKV / Desain Komunikasi Visual</option>
</select>
```

---

<a name="6-textarea-kotak-pesan-panjang"></a>
## 6. 📄 Textarea: Kotak Pesan Panjang

Input `type="text"` hanya muat 1 baris. Jika kamu ingin pengguna menulis cerita, alamat lengkap, atau pesan kesan yang panjang berbaris-baris, gunakan tag `<textarea>`.

```html
<label for="pesan">Alamat Lengkap Rumah:</label><br>
<textarea id="pesan" name="alamat" rows="4" cols="40" placeholder="Ketik alamat rumah lengkap di sini..."></textarea>
```

* `rows="4"` = Tinggi kotak (muat 4 baris teks).
* `cols="40"` = Lebar kotak.

---

<a name="7-button-tombol-kirim--batal"></a>
## 7. 🔘 Button: Tombol Kirim & Batal

Formulir yang sudah diisi butuh tombol aksi untuk menyerahkannya ke server.

```html
<!-- 1. Tombol Kirim (Submit) -->
<button type="submit">🚀 Kirim Pendaftaran</button>

<!-- 2. Tombol Reset / Bersihkan Isi Form -->
<button type="reset">🧹 Bersihkan Form</button>
```

---

<a name="8-validasi-html5"></a>
## 8. 🛡️ Validasi HTML5: Satpam Penjaga Form

HTML5 punya fitur canggih untuk mencegah pengguna mengirim formulir yang kosong atau salah isi, **tanpa perlu nulis kode JavaScript sama sekali!**

### 👮‍♂️ Atribut Satpam Penjaga (Validation Attributes):

1. **`required`**: Mencegah form dikirim jika kotak ini masih kosong (Wajib diisi!).
   ```html
   <input type="text" name="nama" required>
   ```

2. **`placeholder="..."`**: Menampilkan teks petunjuk transparan di dalam kotak (otomatis hilang saat diketik).
   ```html
   <input type="text" placeholder="Contoh: Budi Santoso">
   ```

3. **`minlength` & `maxlength`**: Batas minimal & maksimal jumlah huruf/karakter.
   ```html
   <!-- Password minimal 8 karakter -->
   <input type="password" minlength="8" required>
   ```

4. **`min` & `max`**: Batas minimal & maksimal untuk angka (`number` / `date`).
   ```html
   <!-- Umur harus antara 12 sampai 18 tahun -->
   <input type="number" min="12" max="18">
   ```

5. **`value="..."`**: Mengisi nilai awal secara bawaan/default.
   ```html
   <input type="text" value="Indonesia">
   ```

---

<a name="9-project-seru-mini-form-pendaftaran"></a>
## 9. 🎮 Project Seru: Mini Form Pendaftaran Akademi Gamer & Coding

Mari kita satukan semua ilmu HTML Form hari ini untuk membuat **Formulir Pendaftaran Akademi Pahlawan Digital** yang rapi dan cantik!

### 📝 Salin Kode HTML Ini ke File `index.html`:

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Pendaftaran Akademi Digital</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #0f172a;
            color: #f8fafc;
            padding: 30px;
        }
        .container-form {
            background-color: #1e293b;
            max-width: 550px;
            margin: 0 auto;
            padding: 30px;
            border-radius: 16px;
            border: 2px solid #38bdf8;
            box-shadow: 0 10px 25px rgba(56, 189, 248, 0.2);
        }
        h2 {
            text-align: center;
            color: #38bdf8;
            margin-bottom: 20px;
        }
        .form-group {
            margin-bottom: 18px;
        }
        label {
            display: block;
            margin-bottom: 6px;
            font-weight: 600;
            color: #e2e8f0;
        }
        input[type="text"],
        input[type="email"],
        input[type="password"],
        input[type="number"],
        input[type="date"],
        select,
        textarea {
            width: 100%;
            padding: 10px;
            border-radius: 8px;
            border: 1px solid #475569;
            background-color: #0f172a;
            color: white;
            box-sizing: border-box;
        }
        input:focus, select:focus, textarea:focus {
            outline: none;
            border-color: #38bdf8;
        }
        .radio-group, .checkbox-group {
            display: flex;
            gap: 15px;
            margin-top: 5px;
        }
        .btn-submit {
            width: 100%;
            background-color: #38bdf8;
            color: #0f172a;
            padding: 12px;
            border: none;
            border-radius: 8px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            transition: 0.3s;
        }
        .btn-submit:hover {
            background-color: #f59e0b;
            color: black;
        }
    </style>
</head>
<body>

    <div class="container-form">
        <h2>🚀 Pendaftaran Akademi Pahlawan Digital</h2>
        
        <form action="#" method="POST">
            
            <!-- 1. Input Nama Lengkap -->
            <div class="form-group">
                <label for="nama">Nama Lengkap:</label>
                <input type="text" id="nama" name="nama" placeholder="Ketik nama lengkapmu..." required>
            </div>

            <!-- 2. Input Email -->
            <div class="form-group">
                <label for="email">Alamat Email Aktif:</label>
                <input type="email" id="email" name="email" placeholder="contoh@gmail.com" required>
            </div>

            <!-- 3. Input Password -->
            <div class="form-group">
                <label for="password">Kata Sandi Akun:</label>
                <input type="password" id="password" name="password" minlength="8" placeholder="Minimal 8 karakter" required>
            </div>

            <!-- 4. Input Tanggal Lahir -->
            <div class="form-group">
                <label for="tgl_lahir">Tanggal Lahir:</label>
                <input type="date" id="tgl_lahir" name="tgl_lahir" required>
            </div>

            <!-- 5. Radio Button (Jenis Kelamin) -->
            <div class="form-group">
                <label>Jenis Kelamin:</label>
                <div class="radio-group">
                    <label><input type="radio" name="gender" value="L" required> 👨 Laki-laki</label>
                    <label><input type="radio" name="gender" value="P" required> 👩 Perempuan</label>
                </div>
            </div>

            <!-- 6. Select Dropdown (Pilihan Role / Class) -->
            <div class="form-group">
                <label for="role">Pilih Spesialisasi / Class:</label>
                <select id="role" name="role" required>
                    <option value="" disabled selected>-- Pilih Kelas Keahlian --</option>
                    <option value="frontend">🎨 Front-End Developer (Desainer Web)</option>
                    <option value="backend">⚙️ Back-End Developer (Ahli Server)</option>
                    <option value="gamedev">🎮 Game Developer (Pembuat Game)</option>
                </select>
            </div>

            <!-- 7. Checkbox (Minat Hobi) -->
            <div class="form-group">
                <label>Minat & Hobi (Bisa pilih lebih dari satu):</label>
                <div class="checkbox-group">
                    <label><input type="checkbox" name="hobi[]" value="coding"> 💻 Coding</label>
                    <label><input type="checkbox" name="hobi[]" value="design"> 🖌️ Desain</label>
                    <label><input type="checkbox" name="hobi[]" value="gaming"> 🕹️ Gaming</label>
                </div>
            </div>

            <!-- 8. Input Upload Foto (File) -->
            <div class="form-group">
                <label for="foto">Unggah Pas Foto Avatar:</label>
                <input type="file" id="foto" name="foto" accept="image/*">
            </div>

            <!-- 9. Textarea Alasan -->
            <div class="form-group">
                <label for="alasan">Alasan Ingin Bergabung:</label>
                <textarea id="alasan" name="alasan" rows="3" placeholder="Tuliskan cita-citamu di sini..."></textarea>
            </div>

            <!-- 10. Tombol Submit -->
            <button type="submit" class="btn-submit">🌟 Datar Sekarang!</button>

        </form>
    </div>

</body>
</html>
```

---

<a name="10-rangkuman--kuis-detektif-form"></a>
## 10. 🎯 Rangkuman & Kuis Detektif Form

### 🧠 Cheat Sheet Elemen Form:

| Komponen | Tag / Atribut | Kegunaan |
| :--- | :--- | :--- |
| **Wadah Utama** | `<form action="..." method="...">` | Pembungkus seluruh formulir data |
| **Input Teks** | `<input type="text">` | Kotak isian teks 1 baris |
| **Input Password** | `<input type="password">` | Teks tersembunyi titik-titik (`•••`) |
| **Radio Button** | `<input type="radio" name="x">` | Pilihan tunggal (hanya 1 pilihan) |
| **Checkbox** | `<input type="checkbox">` | Pilihan ganda (bisa centang banyak) |
| **Menu Dropdown** | `<select>` & `<option>` | Pilihan daftar meluncur ke bawah |
| **Pesan Panjang** | `<textarea rows="4">` | Kotak isian teks berbaris-baris |
| **Label Aktif** | `<label for="id_input">` | Menghubungkan teks judul dengan input |
| **Validasi Wajib** | `required` | Mencegah form dikirim jika kosong |
| **Petunjuk Teks** | `placeholder="..."` | Teks transparan bantuan di dalam kotak |

---

### 🧩 Kuis Detektif Form 🕵️‍♂️

Jawab 4 pertanyaan seru ini untuk menguji pemahamanmu:

1. Jika kamu ingin pengguna **HANYA BOLEH MEMILIH SATU** jawaban (seperti Ukuran Baju: S, M, L, XL), tipe input apa yang harus digunakan?
   * a) `type="checkbox"`
   * b) `type="radio"`
   * c) `type="text"`

2. Apa fungsi dari atribut `required` saat dipasang pada tag `<input>`?
   * a) Mengubah warna kotak input jadi merah
   * b) Memaksa kotak input wajib diisi sebelum dikirim
   * c) Menghapus teks secara otomatis

3. Mengapa kita disarankan menghubungkan tag `<label>` dengan `<input>` menggunakan atribut `for` dan `id`?
   * a) Agar jika teks label diklik, kursor mouse otomatis masuk ke dalam kotak input
   * b) Agar tulisan label bisa bergerak
   * c) Agar password tidak bisa dicuri orang

4. Tag apa yang tepat digunakan jika pengguna ingin mengetik **Alamat Lengkap Rumah** yang panjangnya beberapa baris?
   * a) `<input type="text">`
   * b) `<textarea>`
   * c) `<select>`

---

*Kunci Jawaban Kuis: 1. (b), 2. (b), 3. (a), 4. (b)*

**Hebat Sekali! Kamu telah menyelesaikan Pertemuan 3 tentang HTML Form dengan sangat sukses! Sekarang kamu siap melangkah ke Pertemuan 4 untuk menghias semua web ini dengan CSS! 🚀🎨**
