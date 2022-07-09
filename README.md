# Muhamad Iqbal Maulana - IT 02 02 - 1202190023 - Tubes Intergatif

## Instalasi Melalui Komposer (Progress 1)
Jika mesin lokal Anda sudah menginstal PHP dan Composer, Anda dapat membuat proyek Laravel baru dengan menggunakan Composer secara langsung. Setelah aplikasi dibuat, Anda dapat memulai server pengembangan lokal Laravel menggunakan perintah Artisan CLI serve:

Pastikan php yang terinstall sudah versi 7.4 / keatas, maka kita bisa lanjut dengan menginstall composer. Download composer disini [https://getcomposer.org/].

Buka CMD dan jalankan code dibawah ini

```
composer create-project laravel/laravel example-app // Membuat Composer Laravel Baru
 
cd example-app // Masuk ke folder Laravel
 
php artisan serve // Jalankan Laravel
```

Setelah Anda memulai server pengembangan Artisan, Anda dapat mengakses aplikasi Anda di http://localhost:8000.

&nbsp;
## Migrate RSS kedalam Database (Progress 2)
Membuat Sebuah Struktur Database Pada Laravel
![image1](https://github.com/miqbalm01/tubes_news/blob/main/assets/migrate_database.PNG)

&nbsp;
Gunakan Fungsi Seeder Untuk Memudahkan Mengambil Data Secara Keseluruhan Dari RSS kedalam Database kita.

&nbsp;
Disini kita menambahkan 3 RSS dari beberapa domain:
- The New Yorker : https://www.newyorker.com/feed/magazine/rss
- Tempo Nasional : https://rss.tempo.co/nasional
- The New York Times : https://www.wired.com/feed
![image1](https://github.com/miqbalm01/tubes_news/blob/main/assets/database_sender.PNG)

&nbsp;
Lalu Buka CMD, Jalankan Code Dibawah ini
```
php artisan migrate --seed // Untuk Menjalankan Seeder
php artisan migrate:fresh --seed // Untuk Memperbarui Seeder setelah dilakukan perubahan
```
Setelah itu maka data dari ketiga RSS tersebut, akan masuk ke dalam Database Kita
![image1](https://github.com/miqbalm01/tubes_news/blob/main/assets/record_database.PNG)

&nbsp;
## Menampilan RSS kedalam Website (Progress 3)
Kita buat halaman post Pada Laravel
![image1](https://github.com/miqbalm01/tubes_news/blob/main/assets/posts.PNG)

&nbsp;
- Hasil Pada Halaman Utama, Menampilkan Berita dari database
![image1](https://github.com/miqbalm01/tubes_news/blob/main/assets/utama.PNG)

&nbsp;
- Halaman Berita The New Yorker
![image1](https://github.com/miqbalm01/tubes_news/blob/main/assets/newyorker.PNG)

&nbsp;
- Halaman Berita Tempo Nasional
![image1](https://github.com/miqbalm01/tubes_news/blob/main/assets/tempo.PNG)

&nbsp;
- Halaman Berita The New York Times
![image1](https://github.com/miqbalm01/tubes_news/blob/main/assets/yorktimes.PNG)
