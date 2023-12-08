`Tugas ini merupakan tugas mata kuliah konsep jaringan  yang di bimbing oleh Bpk. Ferry Astika S`

## Telnet
Teletype Network, disingkat Telnet, adalah protokol aplikasi yang digunakan untuk mengakses  dan menegendalikan perangkat jarak jauh melalui jaringan internet maupun LAN dan bersifat interaktif dua arah. Telnet terdiri dari dua komponen:
1. Protokol itu sendiri yang menentukan abagaimana kedua belah pihak berkomunikasi, dan
2. Aplikasi perangkat lunak yang menjadi penyedia layanan.

### Karakteristik Telnet
Telnet didefinisikan dan diatur oleh dokumen standar RFC 854. Berdasarkan RFC tersebut, beberapa karakteristik utama dari Telnet adalah sebagai berikut:
- Text-Based: Telnet adalah protokol berbasis teks, yang mana semua datanya dikirim dalam bentuk teks. Pesan di Telnet diakhiri dengan karakter garis baru(Carriage Return dan Line Feed atau CR-LF).
- Karakter Kontrol: Telnet mendefinisikan sejumlah karakter kontrol yang digunakan untuk mengirim perintah khusus kepada server atau untuk mengendalikan perilaku terminal. Contohnya adalah karakter untuk menghapus layar, mengatur atribut teks, atau menggulir layar.
- Negosiasi Opsi: RFC 854 memungkinkan untuk negosiasi opsi antara Telnet client dan server.  Ini berarti client dan server dapat berkomunikasi dan menentukan fitur-fitur tambahan yang akan mereka dukung. Misal, opsi untuk otentikasi pengguna dan negosiasi fitur-fitur tambahan antara client dan server (misalnya, pengaturan terminal atau pengiriman karakter khusus).

### Komponen Telnet
Telnet, seperti yang sudah disebut sebelumnya, terdiri atas dua komponen yaitu:
- Protokol: format komunikasi yang digunakan oleh aplikasi Telnet untuk berkomunikasi dengan perangkat jarak jauh melalui jaringa diatur dalam protokol Telnet. Protokol ini mendefinisikan bagaimana perintah dan data dikirimkan antar Telnet client, yaitu aplikasi, dan Telnet server, yakni perangkat jarak jauhnya. RFC 854 mengatur protokol ini, dimanan terdapat rincian spesifikasi dasar untuk protokol ini.
- Aplikasi: disebut juga sebagai "Telnet client", aplikasi telnet adalah aplikasi yang digunakan oleh pengguna layanan telnet untuk menjalankan sesi telnet dan berinteraksi dengan perangkat jarak jauh. Aplikasi ini memungkinkan pengguna mengakses perangkat jarak jauh dimana mereka memasukkan nama domain atau IP perangkat yang ingin diakses. Saat sudah terhubung, pengguna akan dapat menjalankan perintah, mengakses file, dan lainnya melalui sebuah interface berbasis teks.
- Keamanan Terbatas: Salah satu kekurangan besar dari Telnet adalah kurangnya keamanan. Data yang dikirim antara client dan server Telnet tidak dienkripsi, sehingga rentan terhadap penyadapan. Karena itu, Telnet tidak cocok untuk digunakan di jaringan yang tidak terlindungi.

### Penggunaan Telnet
Protokol ini adalah salah satu protokol jaringan tertua yang kini sudah tidak digunakan lagi. Pada awal penggunaannya, telnet menyediakan akses pada interface berbentuk command-line pada host yang berjarak jauh. Akan tetapi, karena adanya masalah keamanan yang serius dalam penggunaanya pada jaringan yang terbuka seperti internet, penggunaan untuk hal ini sudah banyak beralih pada penggunaan SSH.

Penggunaan telnet pada jaman sekarang lebih digunakan untuk melakukan debug pada layanan jaringan seperti SMTP, IRC, HTTP, FTP atau POP3 untuk mengirimkan sebuah perintah ke server dan memeriksa responnya. Penggunaan protokol yang lebih tua biasanya hanya terjadi pada kasus dimana untuk mengakses perangkat lama/kuno yang tidak mendukung akan penggunaan protokol modern.