# PERTEMUAN 6: Pengenalan JavaScript dan Selector DOM

**Mata Kuliah:** Web Programming  
**Waktu:** 100 Menit  

## A. TUJUAN PEMBELAJARAN (SUB-CPMK)
Mahasiswa mampu menjelaskan peran JavaScript sebagai bahasa pemrograman sisi klien dan memanipulasi elemen DOM seperti merespons *click event* dan mengubah *class/style*.

## B. DASAR TEORI
1. **Peran JavaScript:** Berjalan di sisi peramban (*browser*) untuk merespons tindakan pengguna secara *real-time* tanpa perlu *reload* halaman dari server.
2. **Selector DOM:** Cara JavaScript memilih elemen HTML. Contoh: `document.getElementById()`, `document.querySelector()`.
3. **Interaktivitas (Event Listener):** Menambahkan "pendengar" kejadian, misalnya saat pengguna menekan tombol (`click`).

## C. LEMBAR KERJA PRAKTIKUM

### 1. Persiapan Elemen HTML
Buka `index.php`, tambahkan struktur berikut di dalam `<main>`:
```html
<button id="btn-interaktif">Lihat Persiapan WordPress</button>
<div id="pesan-sistem" class="pesan-tersembunyi">
    <p><strong>DOM JavaScript Aktif!</strong></p>
</div>
```

### 2. Mekanisme CSS
Di `style.css`, tambahkan class untuk menyembunyikan dan menampilkan pesan:
```css
.pesan-tersembunyi { display: none; }
.pesan-tampil { 
    display: block; 
    background-color: #d1ffd1; 
    color: #179351; 
    padding: 10px;
}
```

### 3. Skrip Interaktivitas JavaScript (DOM)
Tambahkan tag `<script>` tepat di atas penutup `</body>` pada `index.php`:
```javascript
<script>
    const tombol = document.getElementById('btn-interaktif');
    const pesan = document.getElementById('pesan-sistem');

    tombol.addEventListener('click', function() {
        if (pesan.classList.contains('pesan-tersembunyi')) {
            pesan.classList.remove('pesan-tersembunyi');
            pesan.classList.add('pesan-tampil');
            tombol.innerText = 'Sembunyikan Informasi';
        } else {
            pesan.classList.remove('pesan-tampil');
            pesan.classList.add('pesan-tersembunyi');
            tombol.innerText = 'Lihat Persiapan WordPress';
        }
    });
</script>
```
Simpan dan jalankan di *browser*. Klik tombol untuk memverifikasi DOM bekerja.---

