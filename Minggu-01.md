# PERTEMUAN 1: Pengantar Web Developer & Konfigurasi Lingkungan Kerja

**Mata Kuliah:** Web Programming  
**Waktu:** 100 Menit  

## A. TUJUAN PEMBELAJARAN (SUB-CPMK)
Mahasiswa mampu menjelaskan cara kerja dasar web, mengidentifikasi fungsi spesifik HTML, CSS, dan JavaScript, serta menyiapkan lingkungan pengembangan lokal.

## B. DASAR TEORI
1. **Arsitektur Client-Server:** Penjelasan mengenai bagaimana *browser* (Klien) meminta data melalui HTTP Request dan *server* merespons dengan mengirimkan dokumen web.
2. **Pengenalan Tools Web Developer:** Pemahaman esensial mengenai **XAMPP** (menggunakan modul Apache sebagai *web server* & MySQL sebagai *database*) dan ekstensi penunjang di *text editor* **Visual Studio Code (VS Code)**.

## C. LEMBAR KERJA PRAKTIKUM

### 1. Instalasi XAMPP dan Konfigurasi Web Server
1. Unduh installer XAMPP versi terbaru untuk sistem operasi Windows/Mac melalui situs resmi Apache Friends.
2. Lakukan instalasi, disarankan membiarkannya di `C:\xampp` agar mudah diakses.
3. Buka aplikasi **XAMPP Control Panel**.
4. Klik tombol **Start** pada baris modul **Apache** dan **MySQL**. Tunggu hingga indikator warna latar modul berubah menjadi hijau.
5. *(Opsional)* Jika terjadi bentrok port pada Apache, buka menu **Config** > `httpd.conf`, ubah `Listen 80` menjadi `Listen 8080`, lalu *restart* modul Apache.

### 2. Instalasi VS Code dan Ekstensi Live Server
1. Unduh VS Code dari situs resmi (`code.visualstudio.com`) dan lakukan instalasi.
2. Buka aplikasi VS Code, klik ikon **Extensions** (atau `Ctrl+Shift+X`).
3. Cari dan instal ekstensi **Live Server** (dikembangkan oleh Ritwick Dey).

### 3. Pembuatan Folder Proyek dan Pengujian Localhost
1. Buka File Explorer, navigasikan ke direktori `C:\xampp\htdocs`.
2. Buat folder baru dengan nama `lapak_kuliner`.
3. Buka folder tersebut di VS Code melalui menu **File > Open Folder**.
4. Buat file baru bernama `index.php`.
5. Ketikkan struktur HTML sederhana:
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Document</title>
   </head>
   <body>
       <h1>Selamat datang di lapak kuliner</h1>
   </body>
   </html>
   ```
6. Simpan file (`Ctrl+S`).
7. Buka *web browser*, ketikkan URL: `localhost/lapak_kuliner`. Halaman akan menampilkan teks yang baru saja Anda tulis.
