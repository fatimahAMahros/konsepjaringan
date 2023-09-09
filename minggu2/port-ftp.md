## Mengapa FTP dapat menggunakan TCP dan UDP

File Transfer Protocol(FTP) adalah protokol internet yang memungkinkan komputer dalam sebuah jaringan untuk bertukar file secara massal. Pada umumnya FTP menggunakan protokol TCP sebagai metode komunikasi utamanya. TCP digunakan karena pengirimannya yang bersifat reliable dan adanya pengaturan urutan sehingga dapat diapstikan integritas dan kehandalan transfer data. Akan tetapi, secara teori ada variasi implementasi FTP yang juga dapat menggunakan UDP walaupun bukan suatu praktek yang umum.
FTP dapat menggunakan TCP atau UDP karena perancangan protokolnya yang sedemikian rupa sehingga dapat menggunakan salah satu dari keduanya dan memberikan fleksibilitas pada penggunaan protokol berdasarkan kondisi dan kebuutuhan.

- TCP pada FTP
Transmission Control Protocol(TCP) adalah protokol yang diguankan oleh FTP dalam kondisi dimana kahandalan, integritas, dan urutan data yang terjamin menjadi prioritasnya. Contohnya saat melakukan transfer file yang memerlukan pengiriman yang terkontrol, pencegahan hilangnya dat, dan urutan yang akurat.

- UDP pada FTP
Penggunaan User Datagram Protocol(UDP) pada FTP sangat terbatas dan jarang terjadi. Kondisi dimana UDP mungkin digunakan pada FTP salah satunya adalah ketika kecepatan transfer lebih penting dari keamanan file-nya. Selain itu adalah ketika berada pada kondisi jaringan dengan kecepatan rendah atau jaringan yang terbatas.
