# PERTEMUAN 7: Dasar-Dasar PHP dan Variabel Dinamis

**Mata Kuliah:** Web Programming  
**Waktu:** 100 Menit  

## A. TUJUAN PEMBELAJARAN (SUB-CPMK)
Mahasiswa mampu menulis kode dengan sintaks dasar PHP, mendeklarasikan variabel dinamis, serta menerapkan logika pemrograman dasar (percabangan dan perulangan) di dalam halaman HTML.

## B. DASAR TEORI
1. **Penulisan PHP:** Berjalan di sisi *server* (membutuhkan XAMPP/Apache). Skrip diawali dengan `<?php` dan diakhiri `?>`.
2. **Variabel:** Deklarasi menggunakan simbol dolar (`$`).
3. **Percabangan & Perulangan:** Menggunakan sintaks `if-elseif-else` untuk kondisi logika, dan `for()` untuk mencetak elemen secara berulang.

## C. LEMBAR KERJA PRAKTIKUM

### 1. Integrasi Variabel Dinamis
Pada baris **paling atas** file `index.php` (sebelum `<!DOCTYPE html>`), tambahkan:
```php
<?php
    $nama_bisnis = "Lapak Kuliner Nusantara";
    $deskripsi = "Pusat Jajanan UMKM & Ekosistem Bisnis F&B";
    $tahun_sekarang = date("Y");
    $status_operasional = "buka"; // Bisa diubah ke "sibuk" atau "tutup"
    $jumlah_mitra = 5;
?>
```
Ganti teks statis di dalam HTML dengan variabel: `<h1><?php echo $nama_bisnis; ?></h1>`.

### 2. Implementasi Percabangan (If - Else)
Gunakan logika ini untuk menampilkan status toko:
```php
<div class="status-toko">
    <h3>Status Operasional:
    <?php
        if ($status_operasional == "buka") {
            echo '<span style="color: #20bf6b;">Buka & Siap Melayani Pesanan</span>';
        } elseif ($status_operasional == "sibuk") {
            echo '<span style="color: #f39c12;">Pesanan Penuh (Harap Antre)</span>';
        } else {
            echo '<span style="color: #eb3b5a;">Tutup Sementara</span>';
        }
    ?>
    </h3>
</div>
```

### 3. Implementasi Perulangan (For Loop)
Cetak daftar mitra UMKM menggunakan *looping*:
```php
<ul>
    <?php
        for ($i=1; $i <= $jumlah_mitra; $i++) {
            echo "<li>Mitra Lapak Kuliner Cabang Ke-" . $i . "</li>";
        }
    ?>
</ul>
```
Uji di peramban dengan mengakses `localhost/lapak_kuliner/index.php`.

---
### Tambahan Materi: Manipulasi Array dan Konversi ke JSON di PHP

Dalam pengembangan aplikasi web modern, data sering kali tidak hanya dicetak langsung ke dalam elemen HTML, tetapi juga perlu dikirimkan dalam format pertukaran data standar seperti **JSON (JavaScript Object Notation)**, terutama jika akan dihubungkan dengan *frontend* modern atau aplikasi seluler.

* **Fungsi `json_encode()`:** PHP menyediakan fungsi bawaan `json_encode()` untuk mengubah struktur data array (baik *indexed array* maupun *associative array*) menjadi string berformat JSON.
* **Header `application/json`:** Ketika memproses data JSON untuk keperluan API, kita perlu menyertakan perintah `header('Content-Type: application/json');` agar peramban atau klien mengenali bahwa respons data yang dikirim adalah format JSON.

---

### Implementasi pada Lembar Kerja Praktikum PHP

Anda dapat menambahkan kode berikut ke dalam file **`index.php`** untuk memperlihatkan bagaimana perulangan array diproses dan dikeluarkan dalam format JSON:

```php
<?php
// 1. Mendeklarasikan Array Multidimensi (Array di dalam Array) untuk Data Mitra UMKM
$daftar_mitra_array = [
    [
        "id" => 1,
        "cabang" => "Cabang Denpasar",
        "pemilik" => "I Made Aryanta",
        "status" => "Buka"
    ],
    [
        "id" => 2,
        "cabang" => "Cabang Badung",
        "pemilik" => "Ni Luh Putu Anandini",
        "status" => "Sibuk"
    ],
    [
        "id" => 3,
        "cabang" => "Cabang Gianyar",
        "pemilik" => "Kadek Agus Gunawan",
        "status" => "Buka"
    ]
];

// 2. Menggunakan Perulangan (Foreach) untuk membaca array dan menampilkannya dalam format HTML
?>

<div class="daftar-mitra-json" style="margin-top: 20px; padding: 15px; background-color: #f8f9fa; border-left: 5px solid #e15f41;">
    <h3>Daftar Mitra Jaringan (Rendering dari Array PHP):</h3>
    <ul>
        <?php
        foreach ($daftar_mitra_array as $mitra) {
            echo "<li><strong>" . $mitra['cabang'] . "</strong> - Pemilik: " . $mitra['pemilik'] . " (Status: " . $mitra['status'] . ")</li>";
        }
        ?>
    </ul>

    <hr style="margin: 15px 0;">

    <h3>Contoh Output Data Berformat JSON (Simulasi API):</h3>
    <pre style="background-color: #2d3436; color: #dfe6e9; padding: 10px; border-radius: 5px; overflow-x: auto;">
<?php 
// Mengubah array PHP menjadi format JSON yang rapi (JSON_PRETTY_PRINT)
echo json_encode($daftar_mitra_array, JSON_PRETTY_PRINT); 
?>
    </pre>
</div>

```

---

### Penjelasan Singkat:

1. **Array Multidimensi (`$daftar_mitra_array`):** Menyimpan sekumpulan data terstruktur layaknya tabel basis data dalam bentuk kunci (*key*) dan nilai (*value*).
2. **Perulangan `foreach`:** Digunakan secara khusus untuk mengurai data *array* di PHP agar setiap elemen di dalamnya bisa dicetak satu per satu ke dalam daftar HTML (`<ul><li>`).
3. **`json_encode(..., JSON_PRETTY_PRINT)`:** Mengonversi struktur array PHP tersebut menjadi teks JSON dengan indentasi yang mudah dibaca langsung pada halaman web.