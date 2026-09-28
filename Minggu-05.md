Berikut adalah modul pembelajaran dan praktikum lengkap untuk **Pertemuan 5** yang disusun berdasarkan Rencana Pembelajaran Semester (RPS) dan dokumen Petunjuk Praktikum yang tersedia.

---

# MODUL PEMBELAJARAN & PRAKTIKUM: PERTEMUAN 5

**Mata Kuliah:** Web Programming (CBDW-216)

**Topik:** Layouting dengan CSS Box Model dan Flexbox

**Alokasi Waktu:** 100 Menit

---

## A. Capaian Pembelajaran

* **CPMK103:** Mengimplementasikan teknologi digital untuk memvisualisasikan data guna memberikan rekomendasi strategi bisnis yang relevan dan berkelanjutan.


* **Sub-CPMK (CBDW-216-SUBCPMK1032):** Mahasiswa mampu menganalisis setiap elemen HTML sebagai sebuah kotak (*Box Model*) untuk mengelola spasi dan dimensinya, serta mengimplementasikan teknik *layouting* modern menggunakan *Flexbox* untuk menyusun elemen-elemen dalam tata letak satu dimensi.



---

## B. Landasan Teori & Materi Kuliah

1. **Analisis Elemen sebagai Kotak (CSS Box Model)**
* Setiap elemen di dalam HTML pada dasarnya dianggap sebagai sebuah kotak persegi yang mengatur bagaimana elemen tersebut memiliki ruang dan jarak. Komponen pembentuk kotak dari dalam ke luar meliputi:


* **Content:** Isi sebenarnya dari elemen tersebut (seperti teks, gambar, atau data visual bisnis).


* **Padding:** Ruang kosong atau spasi transparan di dalam elemen, berada di antara konten dan batas (*border*).


* **Border:** Garis batas yang mengelilingi padding dan konten.


* **Margin:** Ruang kosong atau spasi transparan di luar batas (*border*) yang digunakan untuk memberi jarak antar elemen satu dengan elemen lainnya.






2. **Properti Display Dasar**
* **Block:** Elemen yang memakan lebar layar secara penuh (100%) dan selalu dimulai di baris baru (contoh: `<div>`, `<h1>`, `<p>`).


* **Inline:** Elemen yang hanya memakan lebar sesuai dengan panjang kontennya dan tidak membuat baris baru (contoh: `<a>`, `<span>`).


* **Inline-block:** Gabungan keduanya, di mana elemen tetap berada dalam satu baris tetapi kita bisa mengatur lebar, tinggi, margin, dan padding-nya.




3. **Pengenalan Layout Modern dengan Flexbox**
* *Flexbox* (Flexible Box) adalah metode *layouting* modern yang sangat efisien untuk meratakan dan mendistribusikan ruang antar elemen dalam sebuah wadah (*container*).


* **Container & Items:** Elemen induk (*container*) diberi properti `display: flex;`, dan elemen anak di dalamnya secara otomatis menjadi *items*.


* **flex-direction:** Mengatur arah susunan elemen anak, apakah ke samping menjadi baris (`row`) atau ke bawah menjadi kolom (`column`).


* **justify-content:** Mengatur perataan elemen secara horizontal atau sejajar dengan sumbu utama (contoh: `space-between` untuk mendorong elemen ke ujung kiri dan kanan).


* **align-items:** Mengatur perataan elemen secara vertikal (contoh: `center` untuk memastikan posisi tepat di tengah secara vertikal).





---

## C. Lembar Kerja & Langkah Praktikum

### Langkah 1: Menyiapkan dan Menghubungkan File CSS

1. Di dalam folder proyek Anda melalui Visual Studio Code, pastikan file **`style.css`** sudah tersedia.


2. Buka file `index.php` (atau `index.html`), lalu pastikan file CSS eksternal tersebut sudah dipanggil di dalam bagian `<head>` melalui tag: `<link rel="stylesheet" href="style.css">`.



### Langkah 2: Styling Dasar (Warna dan Tipografi)

1. Buka file `style.css`, lalu atur properti `font-family`, `color`, dan `background-color` untuk elemen utama (`body`):


```css
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #f5f6fa;
    color: #333333;
}

```



### Langkah 3: Menerapkan CSS Box Model (Margin & Padding)

1. Tambahkan aturan berikut pada file CSS Anda untuk memberikan ruang di dalam elemen `header` dan `main`:


```css
header {
    background-color: #e15f41;
    padding: 20px 40px; /* Padding atas/bawah 20px, kiri/kanan 40px */
    margin-bottom: 20px; /* Margin bawah untuk memberi jarak dengan konten */
}

main {
    padding: 30px; /* Padding ke dalam agar konten tidak menepi */
    background-color: #ffffff;
    border: 1px solid #dddddd; /* Garis batas tipis */
}

```



### Langkah 4: Menerapkan Tata Letak Flexbox pada Navigasi

1. Gunakan properti *Flexbox* pada kontainer `header` agar nama merek dan menu navigasi tersusun rapi secara horizontal dan responsif:


```css
header {
    display: flex; /* Mengaktifkan mode Flexbox */
    flex-direction: row; /* Menyusun secara horizontal */
    justify-content: space-between; /* Mendorong elemen ke ujung kiri dan kanan */
    align-items: center; /* Menyelaraskan posisi vertikal di tengah */
}

```



### Langkah 5: Pengujian Hasil

1. Simpan seluruh perubahan pada file `index.php` dan `style.css`.


2. Muat ulang (*refresh*) halaman di peramban atau jalankan melalui *Live Server*. Pastikan spasi (*margin* dan *padding*) terlihat rapi serta elemen pada header sudah sejajar menggunakan *Flexbox*.
