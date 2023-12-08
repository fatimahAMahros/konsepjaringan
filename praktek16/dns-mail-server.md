`Tugas ini merupakan tugas mata kuliah konsep jaringan  yang di bimbing oleh Bpk. Ferry Astika S`

# Cara Kerja dari DNS dan Email Server

DNS (Domain Name System) dan Server Email merupakan dua elemen yang krusial dalam struktur internet yang beroperasi secara independen namun memiliki keterkaitan.

## Cara Kerja Domain Name System(DNS)
1. DNS Request: Saat pengguna memasukkan nama domain (contoh seperti www.aiueo.com) ke dalam peramban web, komputer pengguna mengirimkan permintaan DNS ke server DNS.
2. DNS Resolution: Server DNS mencari informasi sesuai dengan nama domain yang diminta. Jika informasi tersebut sudah ada dalam cache server DNS, maka informasi itu akan dikembalikan ke komputer pengguna. Jika tidak ada dalam cache, server DNS akan menghubungi server lain untuk mencari informasi yang sesuai.
3. Name Resolution: Informasi yang dikembalikan oleh server DNS berisi alamat IP yang terkait dengan nama domain yang diminta. Ini memungkinkan komputer pengguna untuk mengarahkan permintaan mereka ke alamat IP yang benar.
4. Setelah mendapatkan alamat IP dari server DNS, komputer pengguna dapat membuat koneksi langsung ke server yang diinginkan untuk mengakses situs web atau layanan yang dimaksud.

## Cara kerja Email Server
1. Pengiriman Email: Ketika seseorang mengirim email, klien email mereka akan mengirimkan pesan ke server email pengirim.
2. Verifikasi dan Validasi: Server email pengirim memeriksa alamat email penerima untuk memastikan keabsahannya. Jika valid, email akan dikirim ke server email penerima.
3. Penerimaan oleh Server: Server email penerima menerima email dan memeriksa alamat tujuan. Jika alamat email valid, email akan disimpan dalam kotak masuk penerima.
4. Pengambilan Email: Pengguna dapat menggunakan klien email mereka (seperti Outlook, Gmail, dll.) untuk mengambil email dari server email penerima dan membacanya.
5. Respon Email: Saat pengguna menjawab email, klien email mereka mengirim balasan ke server email mereka, dan siklus ini terus berlanjut.

## Hubungan Domain, DNS Server, dan Mail Server
Dalam proses pengiriman email, hubungan antara domain, DNS server, dan mail server sangat penting. DNS berperan dalam menyediakan resolusi nama domain ke alamat IP server email penerima. Ketika email dikirim, server email pengirim menggunakan DNS untuk menemukan alamat IP server email penerima yang terkait dengan nama domain tujuan. Proses ini memungkinkan email dikirim ke server email yang tepat dan diarahkan ke kotak masuk yang sesuai. Oleh karena itu, keterkaitan antara domain, DNS server, dan mail server memastikan bahwa pengiriman email berjalan lancar dalam infrastruktur internet.

## Kesimpulan
DNS memiliki peran penting dalam pengiriman email dengan menyediakan resolusi nama domain ke alamat IP server email penerima. Ketika email dikirim, server email pengirim menggunakan DNS untuk menemukan alamat IP server email penerima yang terkait dengan nama domain tujuan. Proses ini memungkinkan email dikirim ke server email yang tepat dan diarahkan ke kotak masuk yang sesuai. Oleh karena itu, DNS merupakan komponen krusial yang memastikan pengiriman email berjalan lancar dalam infrastruktur internet.