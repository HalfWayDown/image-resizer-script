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

**Cara Kerja**
   1. Resize ke Lebar 1080:
      Semua gambar PNG dalam folder akan diubah ukurannya jika lebar gambar bukan 1080 piksel, dan disimpan dengan suffix -1080.

   2. Pengecekan Ukuran File:
      Skrip akan memeriksa ukuran file setelah resizing awal. Jika ukuran file lebih dari 2000 KB, skrip akan menurunkan kualitas gambar secara bertahap sampai ukuran file berada di bawah 2000 KB dan memberikan suffix -resized.

   3. Penghapusan File Sementara:
      File dengan suffix -1080 akan dihapus setelah file -resized dibuat.

**Menghentikan Proses**
   Jika Anda perlu menghentikan skrip sebelum selesai, Anda dapat melakukannya dengan menekan Ctrl+C. Skrip akan menampilkan pesan "Operation Canceled. Exiting..." dan berhenti.

**Kontribusi**
   Jika Anda ingin berkontribusi pada skrip ini, silakan buat pull request atau laporan masalah (issue) di repository ini.

**Lisensi**
   Skrip ini dilisensikan di bawah MIT License.
