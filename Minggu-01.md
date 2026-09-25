# MODUL PEMBELAJARAN & PRAKTIKUM: PERTEMUAN 1

**Mata Kuliah:** Web Programming (CBDW-216)

**Topik:** Pengantar Web Developer & Konfigurasi Lingkungan Kerja

**Alokasi Waktu:** 100 Menit (Sesuai RPS: 3 SKS, mencakup Kuliah, Diskusi, dan Praktikum)

---

## A. Capaian Pembelajaran

* **CPMK103:** Mengimplementasikan teknologi digital untuk memvisualisasikan data guna memberikan rekomendasi strategi bisnis yang relevan dan berkelanjutan.


* **Sub-CPMK (CBDW-216-SUBCPMK1031):** Mahasiswa mampu menjelaskan cara kerja dasar web, mengidentifikasi fungsi spesifik HTML, CSS, dan JavaScript, serta menyiapkan lingkungan pengembangan lokal (*teks editor* dan *browser*) untuk memulai proyek web.



---

## B. Landasan Teori & Materi Kuliah

1. **Arsitektur Dasar Web (Client-Server & HTTP Request)**
* Dalam ekosistem web modern, interaksi terjadi antara **Klien (*Browser*)** dan **Server**. Klien mengirimkan permintaan (*HTTP Request*) berupa alamat URL ke server, kemudian server memproses permintaan tersebut dan mengirimkan kembali respons berupa file atau data yang dirender oleh browser.




2. **Komponen Utama Pemrograman Web**
* **HTML (HyperText Markup Language):** Berfungsi sebagai kerangka atau fondasi utama untuk menstrukturkan konten web secara semantik.


* **CSS (Cascading Style Sheets):** Berfungsi sebagai pengatur tata letak dan desain visual (estetika, warna, tipografi).


* **JavaScript:** Bahasa pemrograman sisi klien yang bertugas memberikan fungsionalitas serta interaktivitas dinamis.


* **PHP:** Bahasa pemrograman sisi server yang mengelola logika pemrosesan data dinamis.




3. **Peralatan Pengembang Web (*Tools*) & Alternatif Web Server Lokal**
* **XAMPP (Apache & MySQL):** Perangkat lunak server lokal standar yang digunakan untuk menjalankan server Apache dan manajemen basis data MySQL.


* **Laragon (Alternatif untuk Windows):** Lingkungan pengembangan lokal yang sangat cepat, ringan, dan memiliki fitur *Auto Virtual Hosts* (membuat URL otomatis seperti `[http://lapak-kuliner.test](http://lapak-kuliner.test)`).
* **MAMP (Alternatif untuk macOS & Windows):** Aplikasi server lokal dengan antarmuka yang bersih dan ramah pemula.
* **Local (LocalWP):** Alternatif spesifik yang dioptimalkan untuk pengembangan berbasis WordPress (relevan untuk materi pertemuan selanjutnya).
* **Visual Studio Code (VS Code):** Teks editor utama yang dilengkapi dengan berbagai ekstensi penunjang produktivitas pengkodean.





---

## C. Lembar Kerja & Langkah Praktikum

### Langkah 1: Instalasi Web Server Lokal (Pilihan XAMPP atau Alternatif Laragon)

* **Opsi A (Menggunakan XAMPP):**
1. Unduh dan instal XAMPP, lalu biarkan direktori utama diatur pada `C:\xampp`.


2. Buka **XAMPP Control Panel**, aktifkan modul **Apache** dan **MySQL** hingga indikator berwarna hijau.




* **Opsi B (Menggunakan Alternatif Laragon - *Rekomendasi Windows*):**
1. Unduh dan instal aplikasi **Laragon** (pilih versi *Laragon Full*).
2. Jalankan aplikasi Laragon, lalu klik tombol **Start All**. Laragon otomatis menggunakan direktori `C:\laragon\www\` sebagai direktori proyek lokal.



### Langkah 2: Instalasi VS Code dan Ekstensi Live Server

1. Unduh dan instal Visual Studio Code dari situs resminya.


2. Buka menu **Extensions** (`Ctrl+Shift+X`), cari ekstensi **Live Server**, lalu klik **Install**.



### Langkah 3: Pembuatan Folder Proyek dan Pengujian Localhost

1. Buka direktori sesuai server yang Anda gunakan (`C:\xampp\htdocs\` untuk XAMPP atau `C:\laragon\www\` untuk Laragon).
2. Buat folder baru dengan nama **`lapak_kuliner`**.


3. Buka VS Code, pilih menu `File > Open Folder`, lalu pilih folder `lapak_kuliner` tersebut.


4. Buat file baru di dalamnya dan beri nama **`index.php`**.


5. Ketikkan kode pengujian dasar berikut:
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Uji Coba Lingkungan Kerja</title>
</head>
<body>
    <h1>Selamat Datang di Praktikum Web Programming INSTIKI</h1>
    <p>Lingkungan server lokal dan VS Code berhasil dikonfigurasi.</p>
</body>
</html>

```


6. Simpan file (`Ctrl+S`), lalu akses melalui peramban:
* Jika menggunakan XAMPP: `http://localhost/lapak_kuliner/index.php`.


* Jika menggunakan Laragon: `[http://lapak-kuliner.test](http://lapak-kuliner.test)` atau `http://localhost/lapak_kuliner/index.php`.



---

## D. Evaluasi Pembelajaran

* **Bentuk Asesmen:** Partisipasi dan Aktivitas Diskusi Praktikum.


* **Kriteria & Indikator Penilaian:** Ketepatan mahasiswa dalam menyiapkan lingkungan pengembangan lokal (baik menggunakan XAMPP maupun alternatifnya), mengaktifkan modul server tanpa kendala, serta berhasil menjalankan file uji coba di peramban.


* **Bobot Penilaian:** 10% dari total komponen Partisipasi (Kehadiran & Quiz) untuk pencapaian CPMK103.
