Berikut adalah modul pembelajaran dan praktikum lengkap untuk **Pertemuan 4** dalam format teks Markdown yang dapat langsung Anda salin (*copy*) dengan mudah.

---

# MODUL PEMBELAJARAN & PRAKTIKUM: PERTEMUAN 4

**Mata Kuliah:** Web Programming (CBDW-216)

**Topik:** Dasar-dasar Styling dengan CSS

**Alokasi Waktu:** 100 Menit

---

## A. Capaian Pembelajaran

* **CPMK103:** Mengimplementasikan teknologi digital untuk memvisualisasikan data guna memberikan rekomendasi strategi bisnis yang relevan dan berkelanjutan.


* **Sub-CPMK (CBDW-216-SUBCPMK1032):** Mahasiswa mampu menerapkan aturan *styling* dasar pada halaman HTML untuk mengubah properti visual teks dan latar belakang, dengan memanfaatkan sintaks CSS (*selector* dan properti) serta memahami berbagai metode implementasinya (Inline, Internal, dan Eksternal).



---

## B. Landasan Teori & Materi Kuliah

1. **Analogi HTML dan CSS**
* Jika sebuah website diibaratkan sebagai sebuah rumah, maka **HTML** adalah batu bata, fondasi, dan tiang penyangganya (hanya menentukan struktur). Sedangkan **CSS (Cascading Style Sheets)** adalah desain interiornya seperti cat dinding, warna, ukuran jendela, dan tata letak perabotan.




2. **Sintaks Dasar CSS**
* Rumus dasar penulisan aturan CSS selalu mengikuti pola:
`selector { properti: nilai; }`

* **Selector:** Target elemen HTML yang ingin dihias (contoh: tag `<p>` atau `<h1>`).


* **Properti:** Bagian visual yang ingin diubah (contoh: warna teks atau ukuran huruf).


* **Nilai:** Pilihan dari perubahan tersebut (contoh: warna biru atau ukuran `12px`).






3. **Tiga Cara Menambahkan CSS pada Halaman Website**
* **Inline CSS:** Menulis gaya langsung di dalam tag HTML menggunakan atribut `style=""` (kurang efektif untuk website besar).


* **Internal CSS:** Menulis gaya di dalam bagian `<head>` dokumen HTML menggunakan tag `<style>`.


* **External CSS:** Memisahkan seluruh kode gaya ke dalam file khusus berekstensi `.css` (contoh: `style.css`), lalu menghubungkannya ke file HTML. Ini adalah standar profesional industri digital.




4. **Mengenal Selector Umum CSS**
* **Selector Tag:** Memilih semua elemen berdasarkan nama tag HTML-nya (contoh: `p { ... }`).


* **Selector Class:** Menggunakan tanda titik (`.`) untuk memilih elemen berdasarkan atribut kelas tertentu yang dapat digunakan berulang kali (contoh: `.nama-kelas { ... }`).


* **Selector ID:** Menggunakan tanda pagar (`#`) untuk memilih satu elemen unik yang tidak boleh ada duplikatnya di halaman tersebut (contoh: `#id-unik { ... }`).




5. **Properti Styling Dasar (Teks & Latar Belakang)**
* **Teks:** `color` (warna tulisan), `font-size` (ukuran huruf), `font-family` (jenis huruf), dan `text-align` (perataan teks).


* **Latar Belakang:** `background-color` (warna latar).





---

## C. Lembar Kerja & Langkah Praktikum

### Langkah 1: Membuat File CSS Eksternal

1. Buka folder proyek web Anda di **Visual Studio Code**.


2. Buat file baru di panel *Explorer* sebelah kiri dan beri nama **`style.css`**.



### Langkah 2: Menghubungkan CSS dengan HTML (External CSS)

1. Buka file `index.php` (atau `index.html`) Anda.


2. Di dalam bagian `<head>`, tepat di bawah tag `<title>`, tambahkan tag penghubung berikut:


```html
<link rel="stylesheet" href="style.css">

```



### Langkah 3: Menerapkan Properti Latar Belakang dan Teks (Selector Tag)

1. Buka file `style.css`.


2. Tambahkan kode berikut untuk mengubah warna latar belakang seluruh halaman, jenis huruf, dan warna teks utama:


```css
body {
    background-color: #f4f6f7; /* Warna latar abu-abu terang */
    font-family: Arial, sans-serif; /* Jenis huruf dasar */
    color: #333333; /* Warna teks utama abu-abu gelap */
}

```



### Langkah 4: Menerapkan Selector Class dan ID

1. Kembali ke file `index.php`, pastikan elemen `<header>` dan `<h1>` Anda memiliki atribut kelas dan ID:


```html
<header class="header-profil">
    <h1 id="nama-utama">Profil Bisnis Digital</h1>
</header>

```


2. Buka kembali file `style.css` untuk menghias elemen tersebut secara spesifik:


```css
/* Menggunakan Selector Class untuk menghias header */
.header-profil {
    background-color: #2c3e50;
    text-align: center;
    padding: 20px;
}

/* Menggunakan Selector ID untuk menghias teks nama utama */
#nama-utama {
    color: white;
    font-size: 32px;
}

```



### Langkah 5: Pengujian Hasil

1. Simpan perubahan pada kedua file (`Ctrl + S`).


2. Jalankan proyek melalui *Live Server* di VS Code atau akses via *localhost* di peramban. Pastikan halaman web sekarang telah berubah dengan latar belakang berwarna, teks yang rapi, dan bagian header yang terpusat.



