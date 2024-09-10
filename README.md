# Image Resizer Script

## Deskripsi

Skrip ini digunakan untuk mengubah ukuran gambar PNG dalam folder kerja ke lebar maksimum 1080 piksel, memastikan ukuran file akhir tidak melebihi 2000 KB. Skrip ini secara otomatis menangani resizing gambar dan pengurangan kualitas jika diperlukan, serta membersihkan file sementara yang tidak diperlukan setelah proses selesai.

## Fitur

- Mengubah ukuran gambar PNG ke lebar 1080 piksel.
- Memastikan ukuran file akhir tidak melebihi 2000 KB.
- Mengurangi kualitas gambar secara bertahap jika ukuran file lebih dari 2000 KB.
- Menghapus file dengan suffix `-1080` setelah file dengan suffix `-resized` dibuat.
- Mendukung interupsi dengan Ctrl+C.

## Prerequisites

- Anda perlu memiliki `ImageMagick` terpasang di sistem Anda. Untuk memasangnya, ikuti petunjuk di [situs resmi ImageMagick](https://imagemagick.org/script/download.php).

## Penggunaan

1. **Navigasi ke Folder Kerja**  
   Pindah ke direktori yang berisi gambar PNG yang ingin diubah ukurannya.
   
   ```bash
   cd path/to/your/folder

2. **Jalankan Skrip**
   Jalankan skrip dengan menggunakan perintah berikut:
   ```bash
   ./resize_images.sh
   ```
   
   Pastikan skrip memiliki izin eksekusi. Jika tidak, ubah izin dengan:
   ```bash
   chmod +x resize_images.sh
   ```
