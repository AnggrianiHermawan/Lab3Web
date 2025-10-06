# Laporan Praktikum 3 – Membuat Form (Dropdown & Listbox Multiple Selection)
# **Nama:** Anggriani Hermawan
# **NIM:** 312410175
# **Mata Kuliah:** Pemrograman Web 1
# **Dosen Pengampu:** Agung Nugroho, S.Kom., M.Kom  

 ## Tujuan Praktikum
1. Mahasiswa mampu memahami struktur dasar pembuatan Form pada HTML.  
2. Mahasiswa mampu menampilkan elemen **dropdown menu** dan **listbox multiple selection**.  
3. Mahasiswa mampu menambahkan CSS untuk memperindah tampilan form.

## Langkah-langkah Praktikum

### Langkah 1 – Persiapan File HTML
Buat folder baru dengan nama **Lab3Web**, lalu buat file **`lab3_form.html`**.  
Tulis struktur dasar HTML seperti berikut:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Membuat Form</title>
</head>
<body>
  <header>
    <h1>Membuat Form</h1>
  </header>
</body>
</html>
```
<img width="1920" height="1080" alt="Cuplikan layar 2025-10-06 131613" src="https://github.com/user-attachments/assets/a9da725b-cb86-4e2d-88b1-10349a8ed96f" />

### Langkah 2 – Membuat Struktur Form
Tambahkan tag `<form>` dan `<fieldset>` untuk membungkus elemen form.  
```html
<form action="proses.php" method="post">
  <fieldset>
    <legend>Data Mahasiswa</legend>
    <!-- Elemen form ditulis di sini -->
  </fieldset>
</form>
```
 **Penjelasan:**  
- `<form>` digunakan untuk mengelompokkan input pengguna.  
- `action="proses.php"` adalah file tujuan pengiriman data.  
- `<fieldset>` memberi bingkai, dan `<legend>` memberi judul pada form.
<img width="1920" height="1080" alt="Cuplikan layar 2025-10-06 131731" src="https://github.com/user-attachments/assets/c59be2b3-e54e-4184-b235-2c4830f2c1c8" />

###  Langkah 3 – Menambahkan Input Nama & Alamat
Tambahkan input teks dan textarea seperti berikut:
```html
<p>
  <label for="nama">Nama</label>
  <input type="text" id="nama" name="nama">
</p>

<p>
  <label for="alamat">Alamat</label>
  <textarea id="alamat" name="alamat" cols="20" rows="3"></textarea>
</p>
```
 **Penjelasan:**  
- `<input type="text">` untuk mengisi nama singkat.  
- `<textarea>` digunakan untuk teks panjang seperti alamat.
<img width="1920" height="1080" alt="Cuplikan layar 2025-10-06 132040" src="https://github.com/user-attachments/assets/d9faabbd-af00-47c0-ae05-28d82c2f76f9" />

###  Langkah 4 – Menambahkan Dropdown Menu
Tambahkan elemen dropdown untuk memilih program studi:
```html
<p>
  <label for="prodi">Program Studi</label>
  <select id="prodi" name="prodi">
    <option value="">-- Pilih Program Studi --</option>
    <option value="TI">Teknik Informatika</option>
    <option value="SI">Sistem Informasi</option>
    <option value="RPL">Rekayasa Perangkat Lunak</option>
    <option value="MI">Manajemen Informatika</option>
  </select>
</p>
```
 **Penjelasan:**  
- `<select>` membuat dropdown menu.  
- `<option>` menampilkan setiap pilihan yang bisa dipilih pengguna.
<img width="1920" height="1080" alt="Cuplikan layar 2025-10-06 132114" src="https://github.com/user-attachments/assets/f0aff694-f9c3-419e-b72c-15ff574cda8c" />

### Langkah 5 – Menambahkan Listbox Multiple Selection
Tambahkan elemen listbox seperti berikut:
```html
<p>
  <label for="minat">Bidang Minat</label><br>
  <select id="minat" name="minat[]" multiple size="4">
    <option value="web">Pemrograman Web</option>
    <option value="ai">Kecerdasan Buatan</option>
    <option value="network">Jaringan Komputer</option>
    <option value="database">Basis Data</option>
    <option value="uiux">Desain UI/UX</option>
  </select>
</p>
```
 **Penjelasan:**  
- Atribut `multiple` memungkinkan memilih **lebih dari satu** pilihan.  
- Atribut `size="4"` menampilkan 4 baris secara vertikal.  
- `name="minat[]"` menggunakan tanda `[]` agar data dikirim sebagai **array**.
<img width="1920" height="1080" alt="Cuplikan layar 2025-10-06 132147" src="https://github.com/user-attachments/assets/a5b2c125-47cb-4a9d-b187-cf44207f9ca1" />

### Langkah 6 – Menambahkan Tombol Submit
Tambahkan tombol kirim data:
```html
<p><input type="submit" value="Kirim Data"></p>
```
 **Penjelasan:**  
- Tombol ini digunakan untuk mengirim seluruh isi form ke file `proses.php`.
<img width="1920" height="1080" alt="Cuplikan layar 2025-10-06 134956" src="https://github.com/user-attachments/assets/8f06adb2-3145-46fb-9372-fd1f9b0b6349" />

###  Langkah 7 – Menambahkan CSS
Tambahkan kode CSS di dalam tag `<style>` agar tampilan lebih rapi:
```html
<style>
  form p > label {
    display: inline-block;
    width: 120px;
  }
  form input[type="text"], form textarea, form select {
    border: 1px solid #197a43;
    padding: 3px;
  }
  form input[type="submit"] {
    border: 1px solid #197a43;
    background-color: #197a43;
    color: #ffffff;
    font-weight: bold;
    padding: 5px 15px;
  }
</style>
```
 **Penjelasan:**  
- Memberi warna hijau pada border form.  
- Mengatur jarak dan ukuran tombol kirim agar seragam dan profesional.
<img width="1920" height="1080" alt="Cuplikan layar 2025-10-06 132604" src="https://github.com/user-attachments/assets/a37f00e6-fe9b-4087-8fd3-18a680170e1d" />

---

##  Kesimpulan
- Elemen `<select>` dapat digunakan untuk membuat **dropdown menu** maupun **listbox multiple selection**.  
- Atribut `multiple` memungkinkan pengguna memilih **lebih dari satu item**.  
- Dengan menambahkan CSS, tampilan form menjadi lebih menarik dan mudah dibaca.  

---
