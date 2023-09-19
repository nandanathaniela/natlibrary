## ---Tugas 2---
---

# Tautan aplikasi : https://natlibrary.adaptable.app

## **Pengimplementasian checklist secara step-by-step**
Langkah-langkah : Membuat direktori dan repository baru, kemudian membuat proyek Django dan aplikasi baru dengan nama natlibrary, menambahkan ‘main’ ke direktori settings.py sehingga ada direktori baru yaitu main didalam direktori utama, membuat main.html di direktori tersebut, mengubah models.py sesuai ketentuan soal kemudian menjalankan perintah migrasi, menghubungkan view dengan template  dengan menambahkan function pada views.py, mengubah-ubah routing urls sesuai dengan ketentuan dan path yang sesuai, deploy aplikasi di adaptable.io, terakhir add commit push ke dalam github.

##  **Bagan yang berisi request client ke web aplikasi berbasis Django beserta responnya**
<img src="/image//bagan.jpeg">
Dalam aplikasi Django, ketika seorang pengguna mengirim permintaan ke URL tertentu, berkas urls.py akan mencocokkan URL tersebut dengan fungsi views yang sesuai. Fungsi views di views.py akan mengelola logika bisnis dan berkomunikasi dengan model database yang didefinisikan di models.py jika perlu. Kemudian, data yang diperoleh dari model dapat dimasukkan ke dalam berkas HTML templates untuk merender tampilan halaman web. Respons HTML yang dihasilkan dikirimkan kembali ke pengguna, dan browser klien merender halaman web sesuai dengan respons yang diterima. Dengan demikian, aplikasi Django mengatur aliran informasi dan tampilan dalam respons terhadap permintaan pengguna.

## **Mengapa menggunakan Virtual Environment? Apakah tetap dapat membuat tanpa Virtual Environment?**
Virtual environment digunakan untuk mengisolasi proyek karena pemisahan tugas yang jelas sehingga kode menjadi lebih terorganisir, kode juga dapat digunakan kembali dalam berbagai aplikasi yang berbeda, menghindari perubahan tidak sengaja, dan mendukung skalabilitas perkembangan komponennya. Pembuatan aplikasi web berbasis Django tanpa virtual environment memungkinkan namun tidak disarankan untuk meningkatkan pengelolaan dependensi dan menjaga proyek tetap terorganisir dan bebas dari konflik.

## **MVC, MVT, MVVM**
MVC adalah sebuah desain arsitektur perangkat lunak yang memisahkan aplikasi menjadi tiga komponen utama: Model (menangani logika data), View (menangani tampilan), dan Controller (mengatur aliran kontrol). MVC digunakan terutama dalam pengembangan perangkat lunak desktop dan web.
MVT adalah varian dari MVC yang khusus digunakan dalam kerangka kerja web Django, dengan penekanan pada penggunaan Template untuk merender tampilan. Model dan view mirip dengan MVC, tetapi Template digunakan untuk mengatur tampilan HTML dengan menggunakan sintaks Django.
MVVM adalah arsitektur yang sering digunakan dalam pengembangan aplikasi berbasis klien, seperti aplikasi mobile dan aplikasi web yang memanfaatkan JavaScript. Model, view, dan viewmodel adalah komponen utama. MVVM memungkinkan pengikatan data dua arah, yang mempermudah sinkronisasi antara tampilan dan data.

---
## ---Tugas 3---
---
## **Perbedaan antara form POST dan form GET dalam Django**
POST = nilai variabel tidak ditampilkan di URL sehingga lebih aman dan digunakan untuk mengirim data-data penting
GET = nilai variabel ditampilkan di URL sehingga user data dengan mudah memasukkan variable baru dan digunakan untuk mengirim data-data tidak penting

## **Perbedaan utama antara XML, JSON, dan HTML dalam konteks pengiriman data**
Perbedaan inti antara tiga format ini adalah bahwa XML dan JSON digunakan untuk penyimpanan dan pengiriman data, sementara HTML digunakan untuk mengatur tampilan data.  XML digunakan untuk representasi data struktural dan pertukaran data antar sistem, JSON digunakan untuk pertukaran data web yang ringkas dan mudah dibaca. Dengan kata lain, HTML adalah kerangka utama dalam pengembangan web yang menentukan struktur halaman, sedangkan XML atau JSON berfungsi sebagai pengangkut data antara server dan sering digunakan bersama HTML atau aplikasi lainnya.

### Mengapa JSON sering digunakan dalam pertukaran data antara aplikasi web modern?**
JSON lebih mudah dibaca dalam bentuk yang diperluas dibandingkan XML, JSON dapat memiliki jumlah karakter yang jauh lebih rendah, sehingga mengurangi overhead dalam transfer data, JSON jauh lebih mudah untuk diurai.

## **Pengimplementasian checklist secara step-by-step**
Diawali dengan membuat base.html sbagai kerangka umum dan memasukkannya ke dalam templates. Kemudian menambahkan struktur form untuk menerima data produk baru. Membuat fungsi baru di dalam create product didalam views.py yang akan menerima permintaan (request) sebagai parameter dan menghasilkan formulir yang berfungsi untuk menambahkan data. Setelah itu, melakukan perubahan pada fungsi "show_main" yang sudah ada. Selanjutnya, menambahkan jalur (path) baru untuk mengakses fungsi baru yang telah dibuat. Selanjutnya, membuat file HTML baru yang berperan dalam menampilkan formulir yang telah dibuat, dan melakukan modifikasi pada berkas main.html. Setelah itu, tambahkan fungsi-fungsi yang akan diimplemetasikan dalam bent XML dan JSON . Dilanjutkan dengan menambahkan jalur/routing baru untuk akses ke fungsi-fungsi tersebut. Setelah itu, tambahkan fungsi-fungsi untuk mengembalikan data berdasarkan ID dalam bentuk XML dan JSON. Kemudian, tambahkan jalur-jalur baru pada berkas urls.py sesuai dengan fungsi-fungsi baru yang telah dibuat.

## **Screenshot dari hasil akses URL pada Postman**
HTML
<img src="/image//HTML.png">
XML
<img src="/image//XML.png">
JSON
<img src="/image//JSON.png">
XML by ID
<img src="/image//XML by ID.png">
JSON by ID
<img src="/image//JSON by ID.png">