# PERTEMUAN 2 & 3: Struktur Dasar dan Elemen Fundamental HTML

**Mata Kuliah:** Web Programming  
**Waktu:** 100 Menit  

## A. TUJUAN PEMBELAJARAN (SUB-CPMK)
Mahasiswa mampu membangun sebuah halaman web statis dengan struktur yang logis dan semantik, melalui penerapan elemen-elemen HTML fundamental untuk menyajikan konten (teks, list, gambar, dan tautan).

## B. DASAR TEORI
1. **Struktur Dasar Dokumen HTML:** Terdiri dari deklarasi `<!DOCTYPE html>`, `<html>`, `<head>` untuk metadata, dan `<body>` untuk konten utama.
2. **Tag Fundamental:** Heading (`<h1>` - `<h6>`) dan Paragraf (`<p>`).
3. **Tautan dan Media:** Tautan menggunakan tag `<a>` dengan atribut `href`. Media disisipkan menggunakan tag `<img>` dengan atribut `src` dan `alt`.
4. **Daftar (List):** `<ul>` (Unordered List), `<ol>` (Ordered List), dan `<li>` (List Item).
5. **HTML Semantik:** Penggunaan `<header>`, `<main>`, `<nav>`, dan `<footer>` untuk membantu SEO dan kemudahan membaca kode.

## C. LEMBAR KERJA PRAKTIKUM

### Pembuatan Struktur Halaman Profil Menggunakan Semantic HTML
1. Buka folder `lapak_kuliner` di VS Code.
2. Buat folder baru bernama `assets` di dalamnya, lalu simpan file foto profil Anda (misal: `foto_profile.jpg`) ke dalam folder tersebut.
3. Buka `index.php` (atau `index.html`), gunakan tanda seru `!` lalu tekan `Tab` untuk membuat kerangka dasar HTML5.
4. Terapkan **HTML Semantik** dan media:
   ```html
   <body>
       <header>
           <h1>I Made Subrata Sandhiyasa</h1>
           <p>Mahasiswa Bisnis Digital - INSTIKI</p>
       </header>
       <main>
           <img src="assets/foto_profile.jpg" alt="Foto Profil">
           <h3>Daftar Keahlian & Layanan Bisnis</h3>
           <ul>
               <li>Pengembangan Web (Next.js, React, Laravel)</li>
               <li>Manajemen Basis Data (MySQL)</li>
           </ul>
       </main>
       <footer>
           <p>&copy; 2026 Hak Cipta Dilindungi.</p>
           <a href="https://www.linkedin.com" target="_blank">Profil LinkedIn</a>
       </footer>
   </body>
   ```
5. Simpan dan jalankan di *browser*. Pastikan gambar dan tautan berfungsi normal.
