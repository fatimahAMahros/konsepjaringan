`Tugas ini merupakan tugas mata kuliah konsep jaringan  yang di bimbing oleh Bpk. Ferry Astika S`

## Versi HTTP dan Penggunaan TCP Keep-Alive
Koneksi TCP, selalu diawali dan diakhiri dengan sebuah *three-way handshake* dimana client dan server saling mengirim sinyal dalam pembuat an sebuah koneksi. Hal ini dapat memakan waktu yang cukup banyak apabila setiap segmen/request perlu menggunakan sesi yang berbeda-beda.<br>
HTTP persistent connection, atau kerap dikenal HTTP keep-alive adalah sebuah konsep dimana satu koneksi TCP digunakan untuk mengirimkan dan menerima beberapa request/respon HTTP daripada membuat sebuah koneksi baru untuk setiap pasangan requst/respon.
Mekanisme keep-alive ini dirancang untuk mengurangi latensi requst secara jelas karena client tidak perlu melakukan ulang *TCPthree-way handshake* setelah setiap request. Dengan ini, secara umum, koneksi menjadi lebih cepat seiring waktu karena mekanisme TCP yang  *slow-start*.

### HTTP/0.9
Pada HTTP/0.9, koneksi TCP/IP yang digunakan selalu ditutup setelah setiap respon dari server diterima, sehingga untuk setiap pasangan requst/respon harus dibuatkan sebuah sesi TCP/IP baru.

### HTTP/1.0
Pada HTTP versi 1.0, koneksi masih bersifat seperti pada HTTP 0.9, dimana koneksi harus ditutp setelah setiap pasangan requst/respon. Akan tetapi, pada akhir 1996, banyak developer prodok populer(seperti browser, web server, dsb.) mulai menggunakan sebuah ekstensi tidak resmi pada protokol dengan nama "keep-alive" sehingga memungkinakn penggunaan sebuah koneksi untuk beberapa pasangan request/respon.

### HTTP/1.1
Pada HTTP 1.1, mekanisme keep-alive resmi diperkenalkan sehingga satu sesi TCP/IP dapat digunakan untuk beberapa request/respon. Hal ini menjadikan semua koneksi sebagai persistent connection kecuali dinyatakan sebaliknya. Koneksi ini sudah tidak menggunakan pesan keep-alive yang terpisah, melainkan memungkinkan untuk terkirimnya beberapa request menggunakan satu koneksi saja. akana tetapi, waktu timeout dari koneksi berkisar pendek(5-15 detik).
Pada HTTP 1.1 ini mulai diterapkan pipelining yang berfungsi untuk mengurangi lag sehingga memungkinkan client untuk mengirimkan beberapa request tanpa perlu jmenunggu adanya balasan. AKan tetapi, optimalisasi ini dianggap tidak terlalu aman karena banyaknya server proxy yang tidak menangani request dengan pipeline ini dengan benar, mengakibatkan ketidakakuratannya data. isalnya, jika server harus mengirimkan tanggapan dari permintaan pertama dalam urutan yang tidak sesuai dengan urutan permintaan aslinya, ini dapat menyebabkan masalah. Selain itu, jika salah satu permintaan dalam pipelining mengalami kesalahan, itu dapat mempengaruhi permintaan lainnya dalam antrian.

### HTTP/2
Pada HTTP 2, penggunaan persistent connections diperluas dengan adanya mulpiplexing dimana beberapa request dapat dikirimkan secara bersamaan dan respon tidak harus diterima secara berurutan.
Pada multiplexing, permintaan dan tanggapan dibagi menjadi kerangka data kecil yang diberi nomor urut. Kedua sisi (klien dan server) dapat mengirim dan menerima kerangka data ini secara asinkron melalui satu koneksi, sehingga tidak ada blokade atau konflik yang mungkin terjadi. Perbedaannya dengan pipeline terletak pada fleksibilitas dan efisiensinya, dimana pipeline mengharuskan urutan permintaan dan tanggapan yang sesuai, sedangkan multiplexing memungkinkan keduanya bergerak secara independen dan tidak harus mengikuti urutan yang sama

### HTTP/3
HTTP 3 menggunakan protokol transportt QUIC, yang dirancang untuk mengoptimalkan koneksi internet yang lambat dan tidak stabil.Seperti pada HTTP 2, HTTP 3 juga mendukung penggunaan multiplexing dan persistent connection. Perbedaannya terdapat pada HTTP 3 yang berfokus pada mengatasi maslah latensi yang penting untuk sebuah aplikasi web yang interaktif. Dalam beberapa kasus, QUIC ini memungkinkan pengiriman data yang lebih cepat dan efisien dibandingkan dengan TCP.
<p align="center">
<img src="../assets/http-versions.png" alt="ilustrasi koneksi TCP pada setiap veri HTTP">
<i>Gambar: Ilustrasi koneksi TCP pada setiap versi HTTP</i>
</p>