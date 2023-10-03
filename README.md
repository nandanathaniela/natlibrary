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


---
## ---Tugas 3---
---
## **Apa itu Django UserCreationForm, dan jelaskan apa kelebihan dan kekurangannya?**
UserCreationForm disediakan oleh Django untuk memudahkan pengembang web dalam mengimplementasikan fungsionalitas otentikasi pengguna (user authentication) dalam aplikasi untuk membuat akun pengguna dengan informasi dasar seperti nama pengguna (username), alamat email, dan kata sandi (password).
kelebihan = mudah dan fleksibel
kekurangan = fitur terbatas, tampilan default, rentan serangan

## **Apa perbedaan antara autentikasi dan otorisasi dalam konteks Django, dan mengapa keduanya penting?**
Autentikasi adalah proses verifikasi identitas pengguna. Otorisasi adalah proses yang menentukan apa yang diizinkan atau tidak diizinkan pengguna lakukan setelah mereka berhasil terautentikasi. Keduanya penting dalam menjaga keamanan dan privasi data pengguna. Jika tidak ada autentikasi, kemungkinan besar akun-akun akan menjadi rentan terhadap peretasan oleh pengguna lain. Sementara itu, tanpa otorisasi, ada potensi bahwa pengguna dapat mengakses informasi pribadi yang seharusnya hanya dapat diakses oleh admin atau pemilik aplikasi.

## **Apa itu cookies dalam konteks aplikasi web, dan bagaimana Django menggunakan cookies untuk mengelola data sesi pengguna?**
Cookies adalah data yang disimpan pada perangkat saat pengguna berinteraksi dengan aplikasi web. Dalam dunia aplikasi web, cookies berfungsi sebagai penyimpanan sementara pada perangkat pengguna, dan dapat digunakan untuk mengidentifikasi pengguna yang telah terotentikasi, pelacakan preferensi pengguna serta pengelolaan data sesi pengguna. 
Ketika pengguna masuk ke dalam aplikasi, Django membuat ID unik dan menyimpannya dalam cookie. Kemudian, ketika pengguna melakukan hal lain di aplikasi, Django dapat mengenali pengguna berdasarkan cookie ini dan mengambil data pengguna yang tersimpan di server, seperti keranjang belanja. Namun, sesi ini biasanya memiliki waktu kadaluwarsa yang dapat dikonfigurasi. Ini berarti data sesi akan tetap tersedia selama sesi tersebut masih aktif dan cookie sesi belum kadaluwarsa.

## **Apakah penggunaan cookies aman secara default dalam pengembangan web, atau apakah ada risiko potensial yang harus diwaspadai?**
Penggunaan cookies dalam pengembangan web tidak selalu aman secara otomatis. Ada beberapa risiko, seperti data yang tidak aman, pelacakan pengguna, atau serangan.

## **Pengimplementasian checklist secara step-by-step**
Diawali dengan mengimpor modul yang diperlukan dan membuat fungsi register, login, logout. Membuat implementasi fungsi-fungsi tersebut, membuat berkas html register dan login, mengimpor dan menambahkan path pada urls dari ketiga fungsi. Kemudian menambahkan kode di atas fungsi show_main agar halaman main hanya dapat diakses oleh pengguna yang terautentikasi. Tambahkan informasi cookie last login pada halaman web untuk menambahkan cookie dan menghapus cookie saat pengguna logout. Terakhir, hubungkan model Item dengan user sehingga hanya pengguna yang sedang terotorisasi yang bisa melihat produk-produk yang telah dibuat sendiri degan menambahkan kode pada untuk foreignkey pada models.py.

---
## ---Tugas 3---
---

## **Jelaskan manfaat dari setiap element selector dan kapan waktu yang tepat untuk menggunakannya.**
Type selector : menargetkan objek yang termasuk dalam elemen tersebut atau menerapkan sesuatu pada semua subjek dari elemen tertentu tersebut
Class selector : menargetkan objek yang memiliki atribut kelas yang sama atau menerapkan modifikasi pada objek yang termasuk dalam kelas yang sama
ID selector : menargetkan elemen yang memiliki ID tunggal yang sama

## **Jelaskan HTML5 Tag yang kamu ketahui**
<title>: digunakan untuk menentukan judul halaman web yang akan ditampilkan di judul browser
<a>: digunakan untuk membuat tautan ke halaman web lain
<img>: menampilkan gambar di halaman web
<table>: digunakan untuk membuat tabel yang mengandung data dalam baris dan kolom
<div>: digunakan untuk mengelompokkan dan mengatur konten secara visual atau untuk menerapkan gaya CSS
<nav>: digunakan untuk mengelompokkan elemen-elemen yang berisi menu navigasi

## **Jelaskan perbedaan antara margin dan padding**
Padding: mengosongkan area di sekitar konten (transparan), mengatur ruang di dalam elemen, seperti mengendalikan jarak antara konten dan tepi elemen
Margin: mengosongkan area di sekitar border (transparan), mengatur jarak antara elemen-elemen dalam tata letak atau mengendalikan ruang di sekitar elemen

## **Jelaskan perbedaan antara framework CSS Tailwind dan Bootstrap. Kapan sebaiknya kita menggunakan Bootstrap daripada Tailwind, dan sebaliknya?**
Tailwind CSS menawarkan fleksibilitas tinggi dengan pendekatan "utility-first" yang memungkinkan tingkat kustomisasi yang tinggi, sementara Bootstrap hadir dengan banyak komponen UI siap pakai yang mempercepat pengembangan proyek tetapi dengan kustomisasi yang lebih terbatas. Bootstrap lebih cocok untuk proyek yang memerlukan pembuatan cepat dengan komponen standar, sementara Tailwind lebih sesuai untuk proyek yang memerlukan desain yang sangat disesuaikan dan minimalis. 

## **Pengimplementasian checklist secara step-by-step**
Diawali dengan menambahkan kode bootstrap CSS dan JS. Kemudian menambahkan kode untuk navbar di main.html. Menambahkan fitur edit product dan delete product dengan dengan membuat fungsi, membuat path url, dan membuat button seperti tugas-tugas sebelumnya. Terakhir, tambahkan dan modifikasi kode untuk mempercantik tampilan web di dalam folder static/css sesuai dengan halaman-halaman web.