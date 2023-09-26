## SSH
Secure Shell Protocol, dikenal juga sebagai SSH, adalah protokol jaringan kriptografi yang digunakan untuk mengoperasikan layanan jarinagn secara aman pada sebuah jaringan terbuka/tidak aman. SSH dirancang pada OS menyerupai Unix, sebagai pengganti dari Telnet dan protokol jarak jauh Unix Shell seperti rsh, rlogin, dan rexec yang menggunakan token autentikasi yang tidak terenkripsi.

### Karakteristik Telnet
- Enkripsi: SSH mengenkripsi semua data yang dikirimkan antara klien dan server, termasuk kredensial login dan perintah yang dieksekusi. Hal ini menjaga data agar tidak dapat dengan mudah dicegat atau dibaca oleh pihak luar.
- Autentikasi: SSH mendukung berbagai metode otentikasi seperti: autentikasi berbasis kata sandi, berbasis kunci publik, dan berbasis sertifikat. Ini memungkinkan verifikasi identitas pengguna atau sistem yang mencobamelakukan koneksi.
- Integritas Data: untuk mendeteksi perubahan atau penyuntingan data yang tidak sah selama transmisi, SSH menggunakan *cryptographic hash*. Hal ini untku memastikan bahwa data yang diterima sama dengan yang dikirimkan.
- Tunneling: SSH memungkinkan pembuatan terowongan aman yang dapat mengalirkan lalu lintas jaringan antara sistem lokal dan sistem jarak jauh yang berguna untuk mengakses layanan dan sumber daya di jaringan jarak jauh secara aman.
- Autentikasi Key-Based: public-key based authentication adalah metode yang sangat aman untuk autentikasi di SSH. Pengguna membuat pasangan kunci (public-key dan private key), dengan private-key disimpan dengan aman di mesin klien dan public-key di server. Ini menghilangkan kebutuhan untuk mengirim kata sandi melalui jaringan.
- Port Default: SSH biasanya menggunakan port 22 untuk komunikasi secara default.

### Penggunaan 
SSH adalah protokol yang bisa digunakan untuk banyak aplikasi di berbagai platform termasuk sebagian besar platform Unix dan juga MS Windows. Beberapa penggunaannya adalah sebagai berikut:
- Untuk login pada host jarak jauh(menggantikan Telnet dan rlogin),
- Mengeksekusi perintah tunggal pada host jarak jauh(menggantikan rsh),
- Melakukan pengaturan login otomatis(tanpa password) ke server jarak jauh,
- Melakukan tunneling,
- Menyimpan file back-up, salinan, dan mirror secara efisien dan aman, dan sebagainya.

### Pervedaan SSH dengan Telnet
SSH dan Telnet sama-sama protokol jarinagn yang keduanya digunakan utnuk mengakses dan mengelola komputer atau serverr secara jarak jauh. Akan tetapi, sempat disinggun sebelumnya bahwa SSH digunakan sebagai pengganti Telnet. Berikut beberapa perbedaan utama antara SSH dan Telnet:
- Keamanan: SSH dirancang dengan keamanan sebagai prioritas utam diamana ia mengenkripsi semua dat ayang dikirimkan antara klien dan server sehingga tahan terhadap adanya penyadapan. Sedangkan, Telnet mengirimkan semua datanay dalam bentuk plain text(tidak terenkripsi) sehingga rentan untuk disadap oleh pihak yang tidak berwenang, menjadikannya tidak aman.
- Autentikasi: SSH mendukung berbagai metode autentikasi yang memungkinkan pengguna untuk memilih metode otentikasi yang sesuai dengan kebutuhan keamanan. Sedangkan Telnet mengandalkan otentikasi berbasis kata sandi saja.
- Integritas Data:  SSH memastikan integritas data dengan menggunakan hash kriptografis untuk mendeteksi perubahan atau penyuntingan data selama transmisi yang mencegah terjadinya perubahan data yang tidak sah. Sedangkan Telnet tidak menyediakan mekanisme untuk memastikan integritas data, sehingga data dapat dimanipulasi oleh pihak yang tidak berwenang.