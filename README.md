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