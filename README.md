Safitri Herdian Rachmawati - 185150700111007


# PENJELASAN

Pada praktikum kali ini kita membuat dan mempersiapkan projek Lumen baru. Selain itu, kita belajar tentang mengimplementasikan controller, migration, seeder, model serta dapat menjalankan aplikasi Lumen.

## MVC
Sebelum menjelaskan struktur yang ada di laravel, saya akan menjelaskan konsep dasar yang digunakan pada praktikum ini, yaitu konsep MVC (Model, View, Controller) yang mendukung desain arsitektur sebuah software atau aplikasi untuk memisahkan antara manipulasi data, antarmuka pengguna dan kontrol aplikasi. Fungsi dari masing-masing konsep tersebut antara lain, Model sebagai penghubung antara controller dengan database yang berguna untuk mengambil data, Controller untuk menerima request dan data dari user untuk menentukan apa yang akan diproses oleh aplikasi, sedangkan View digunakan untuk menerima dan merepresentasikan data kepada user

##
## STRUKTUR LARAVEL
### Controller
Controller adalah salah satu komponen inti dari MVC yang berfungsi sebagai penghubung antara request user (View) ke model yang nantinya akan di kembalikan lagi ke View dalam bentuk response. Controller ini akan banyak berisi logika – logika dalam menyusun suatu fungsi tertentu. Contohnya adalah aktivitas CRUD (Create, Read, Update, Delete) yang prosesnya berjalan di dalam Controller

### Migration
Migration merupakan salah satu fitur Laravel yang berfungsi seperti version control untuk database. Melalui fitur ini sebuah team pengembangan web development akan dapat bekerja dalam team untuk mengelola dan modifikasi skema basis data aplikasi. Struktur migration terdiri dari 2 method up dan down. Method up  dipergunakan untuk menambahkan tabel, columns, atau index pada database. Sebaliknya down dipergunakan untuk mengembalikan status pada posisi sebelum method up dijalankan.

### Seeder
Seeder pada laravel adalah sebuah fitur untuk mengisi data pada database dengan data sembarang atau data testing. Dengan adanya fitur ini, kita bisa menginput data ke database dengan cepat dengan menggunakan fitur perintah php artisan yang ada pada laravel.

### Model
Model merupakan salah satu dari bagian MVC yang akan berkomunikasi dengan database. Model yang sudah terhubung ke database akan digunakan/dipanggil via Controller sebagaimana konsep MVC itu berjalan. Untuk membuat model dapat meggunakan perintah artisan untyk menghasilkan sebuat table dalam database

#
# CHALLENGE
Pada challege kali ini kita membuat CRUD untuk project bookapp yang telah kita kerjakan kemarin menggunakan framework laravel.

## CRUD (Create, Read, Update, Delete)
Operasi CRUD adalah manipulasi dasar yang harus ada pada database. Dengan CRUD, kebutuhan manipulasi data akan terpenuhi. Sebelum mengenal lebih lanjut, alangkah baiknya jika kita sudah mengetahui MVC. 
### Create
Pada tahap ini kita membuat authors baru dengan menjalankan HTTP method POST endpoint /authors 
### Read
Pada tahap ini kita akan menampilkan author secara keseluruhan atau berdasarkan id menggunakan HTTP method GET endpoint /authors atau /authors/{id}
### Update
Pada tahap ini kita dapat memperbaharui data author berdasarkan id yang kita inginkan dengan menjalankan HTTP method PUT endpoint /authors/{id} 
### Delete
Pada tahap ini kita dapat menghapus data author berdasarkan id dengan menjalankan HTTP method DELETE endpoint /authors/{id} 
