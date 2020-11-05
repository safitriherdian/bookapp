Safitri Herdian Rachmawati - 185150700111007


## PENJELASAN

Pada praktikum kali ini kita membuat dan mempersiapkan projek Lumen baru. Selain itu, kita belajar tentang mengimplementasikan controller, migration, seeder, model serta dapat menjalankan aplikasi Lumen.

### Langkah Percobaan
Praktikum ini terdiri dari 9 percobaan, yaitu :

#### 1. Instalasi Projek Lumen
Pada langkah ini, kita membuat project baru dengan nama "bookapp".  Untuk membuat project baru dapat menjalankan perintah : composer create-project --prefer-dist laravel/lumen bookapp

#### 2. Membuat Database
Membuat database baru dengan nama "bookapp_lumen" yang dibuat di http://localhost/phpmyadmin/ dengan user root

#### 3. Environment Setup
Memmbuka file .env pada projek bookapp dan menyesuaikan environment kita. Seperi mengubah APP_NAME menjadi "bookapp", DB_DATABASE menjadi "bookapp_lumen", DB_USERNAME menjadi "root", dan mengosongkan DB_PASSWORD. Setelah itu, melakukan konfigurasi API Key dengan membuka routes/web.php dan membuat function $router /key

#### 4. Mengaktifkan fitur Facades dan Eloquent
Untuk mengaktifkan fitur facades dan eloquent dapat menghilangkan comment pada kode : $app->withFacades(); dan $app->withEloquent(); di file app.php direktori bootstrap

#### 5. Membuat Migration
Menjalankan perintah : php artisan make:migration create_books_table --create=books untuk membuat tabel books pada database bookapp_lumen. Selanjutnya, menyesesuaikan kolom tabel pada migration dengan skema yang ada di modul bab 5. Setelah selesai membuat skema, menjalankan perintah : php artisan migrate. Fungsi perintah tersebut adalah untuk melakukan migration karena sebelumnya telah melakukan perubahan pada file migration

#### 6. Membuat Seeder
Mengubah file DatabaseSeeder.php pada direktori database\seeders dan menyesuaikanya dengan kode yang ada di modul bab 5. Setelah melakukan perubahan dapat menjalankan perintah : php artisan db:seed untuk melakukan seeding ke database

#### 7. Membuat Model
Membbuat model Book pada direktori app\Models dengan mendefinisikan atribut tabel seperti kode yang ada di modul bab 5

#### 8. Memanggil data melalui Model
Mengedit BooksController.php pada direktori app\Http\Controllers dengan kode yang ada di moodul bab 5. Setelah itu membuat route pada route\web.php untuk memanggil function pada BooksController

#### 9. Menjalankan Aplikasi
Menjalankan aplikasi yang sudah dibuat sebelumnya dengan menjalankan perintah : php -S localhost:8000 -t public dan mengakses localhost:8000/books

### Tugas Praktikum
Pada praktikum ini kita menambahkan route /books/{id} dengan menampilkan detail buku sesuai id yang kita inputkan. Selain itu, kita juga membuat pesan "Book Not Found" dan status code "404" jika id yang dimasukkan tidak ditemukan.

## KESIMPULAN
PHP artisan adalah generator laravel yang berfungsi untuk membuat file kodingan dengan mudah, seperti membuat controller, model, seeder, migration dan masih banyak lagi. PHP artisan hanya bisa di lakukan di dalam lingkungan console, seperti cmd dan terminal

### Controller
Controller adalah salah satu komponen inti dari MVC yang berfungsi sebagai penghubung antara request user (View) ke model yang nantinya akan di kembalikan lagi ke View dalam bentuk response. Controller ini akan banyak berisi logika – logika dalam menyusun suatu fungsi tertentu. Contohnya adalah aktivitas CRUD (Create, Read, Update, Delete) yang prosesnya berjalan di dalam Controller

### Migration
Migration merupakan salah satu fitur Laravel yang berfungsi seperti version control untuk database. Melalui fitur ini sebuah team pengembangan web development akan dapat bekerja dalam team untuk mengelola dan modifikasi skema basis data aplikasi. Struktur migration terdiri dari 2 method up dan down. Method up  dipergunakan untuk menambahkan tabel, columns, atau index pada database. Sebaliknya down dipergunakan untuk mengembalikan status pada posisi sebelum method up dijalankan.

### Seeder
Seeder pada laravel adalah sebuah fitur untuk mengisi data pada database dengan data sembarang atau data testing. Dengan adanya fitur ini, kita bisa menginput data ke database dengan cepat dengan menggunakan fitur perintah php artisan yang ada pada laravel.

### Model
Model merupakan salah satu dari bagian MVC yang akan berkomunikasi dengan database. Model yang sudah terhubung ke database akan digunakan/dipanggil via Controller sebagaimana konsep MVC itu berjalan. Untuk membuat model dapat meggunakan perintah artisan untyk menghasilkan sebuat table dalam database
