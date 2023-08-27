# Protokol Komunikasi
<h4>Mata Kuliah Praktikum Konsep Jaringan</h4>
<h4>Politeknik Elektronika Negeri Surabaya</h4>

![Logo PENS](https://upload.wikimedia.org/wikipedia/id/4/44/Logo_PENS.png)
<p>Nama Dosen Pengampu: Ferry Astika Saputra</p>
<p>Oleh:</p>
<p>Nama:   Fatimah Az-zahra' Mahros</p>
<p>NRP:    3122600002</p>
<p>Kelas:  2 D4 ITA</p>
## Protokol Model OSI
<p>Model OSI (Open Systems Interconnection) adalah model referensi yang digunakan untuk memahami dan menggambarkan cara komunikasi jaringan komputer berlangsung. Model ini dibuat oleh ISO (International Organization for Standardization) pada tahun 1984 sebagai cara untuk menggambarkan dan memahami berbagai komponen yang terlibat dalam proses komunikasi jaringan dengan tujuan untuk mempermudah pemahaman terhadap komunikasi jaringan yang kompleks dengan memecahnya menjadi beberapa lapisan. Model ini terdiri dari 7 lapisan atau layer yang masing-masing layernya memiliki fungsinya sendiri yakni: physical, data link, network, transport, session, presentation, dan aplication.</p>

![Ilustrasi Model OSI](https://upload.wikimedia.org/wikipedia/commons/thumb/4/47/Osi-model-jb.svg/808px-Osi-model-jb.svg.png?20150501092329)
*<p>Gambar: Ilustrasi lapisan pada model OSI(Sumber: Wikimedia Commons)</p>*

<p>Berikut penjelasan dari setiap layer yang ada pada protokol OSI:</p>

1. Applikation layer(lapisan ke-7)
Lapisan paling atas ini berfungsi sebagai interface dengan aplikasi dengan fungsionalitas jaringan, mengatur bagaimana aplikasi dapat mengakses jaringan, dan membuat error message. Protokol yang digunakan dalam layer ini diantara lainnya adalah HTTP, FTP, DNS, IMAP, dan lainnya. Antara protokol yang digunakan oleh sender dan receiver haruslah sama(contoh: sender menggunakan HTTP, maka receiver juga harus menggunakan HTTP).

2. Presentation Layer(lapisan ke-6)
Lapisan ini berfungsi untuk menerjemahkan data yang hendak ditransmisikan oleh aplikasi ke dalam format yang dapat ditransmisikan melalui jaringan. Layer in bertanggung jawab untuk memastikan semua data yang berasal dari application layer dapat dibaca pada sistem lainnya. Pada layer ini, data akan ter-enkripsi dan dekripsi secara otomatis melalui sistem.

3. Session Layer(lapisan ke-5)
LApisan ini berfungsi untuk mendefinisikan bagaimana koneksi dapat dibuat, dipelihara, atau dihancurkan. Lapisan ini juga bertanggung jawab untuk membuka session dan memastikannya tetap terbuka ketika data sedang dikirim. Selanjutnya apabila komunikasi sudah berakhir, layer session yang akan menutup sessions lagi. Tak hanya itu, lapisan ini juga mengatur checkpoint selama proses transfer. Apabila session terganggu, perangkat dapat melanjutkan transfer data dari checkpoint terakhir. Protokol yang digunakan di layer ini adalah TCP.

4. Transport Layer(lapisan ke-4)
Lapisan ini berfungsi untuk memecah data(segmentasi) ke dalam paket-paket data serta memberikan nomor urut ke paket-paket tersebut sehingga dapat disusun kembali pada sisi tujuan setelah diterima. Selain itu, pada tingkat ini juga membuat sebuah tanda bahwa paket diterima dengan sukses, dan mentransmisikan ulang terhadap paket-paket yang hilang di tengah jalan. Protokol yang digunakan di layer ini adalah TCP dan UDP, dimana TCP menangani koneksi yang dapat diandalkan user sedangkan DPU lebih cepat tapi tidak memiliki jaminan pengiriman.

5. Network Layer(lapisan ke-3)
LApisan ini berfungsi untuk mendefinisikan alamat IP sehingga setiap komputer dapat saling terkoneksi dalam satu jaringan. Fungsi lainnya adalah membagi data menjadi beberapa paket lalu mengembalikannya setelah data berhasil diterima.Protokol yang digunakan di layer ini adalah IP dan IPX.

6. Data Link Layer(lapisan ke-2)
Lapisan ini berfungsi untuk menentukan bagaimana bit-bit data dikelompokkan menjadi format yang disebut sebagai frame yang berhubungan dengan hardware kemudian didistribusikan melalui media. Selain itu, layer ini juga berfungsi untuk memeriksa apabila terjadi kesalahan dalam menyalurkan transmisi terhadap bit data, melakukan koreksi kesalahan, flow control, serta pengalamatan perangkat keras. Protokol yang digunakan di layer ini adalah ARP dan RARP.

7. Physical Layer(lapisan ke-1)
Lapisan ini berfungsi untuk mentransmisikan data dalam bentuk bit stream. Adapun jenis sinyal yang dipakai pada lapisan ini tidak boleh sembarangan dan jenisnya pun harus didukung media fisik, seperti fiber optik, gelombang radio, dan kabel listrik.

## TCP/IP
<p>TCP/IP(Transmission Communication Protocol/Internet Protocol) adalah salah satu protokol jaringan yang menjadi standar komunikasi data dalam jaringan komputer dan digunakan untuk proses pertukaran data antar perangkat, biasanya yang terhubung melalui jaringan internet. Protokol ini dikembangkan sejak akhir 70-an hingga awal 80-an untuk membentuk sebuah WAN. Protokol ini menggunakan skema pengalamatan yang sederhana yaitu IP sehingga memunkinkan berjuta-juta komputer untuk dapat saling berhubungan satu sama lainnya melalui Internet. Berbeda dengan model OSI yang pada arsitekturnya memiliki 7 lapisan, TCP/IP hanya memiliki 4 lapisa tapi dapat dipetakan kembali terhadap model OSI. Keempat lapisan tersebut adalah: application, transport, network, network interface.</p>

![](https://media.geeksforgeeks.org/wp-content/uploads/20230417045622/OSI-vs-TCP-vs-Hybrid-2.webp)
*<p>Gambar: Ilustrasi antara model OSI dengan TCP/IP(Sumber: Geeksforgeeks)</p>*

<p>Berikut penjelasan dari setiap layer pada TCP/IP:</p>

1. Application Layer(lapisan ke-4)
Lapisan ini berfungsi untuk menyediakan akses untuk aplikasi terhadap layanan jaringan dari TCP/IP. Lapisan ini memiliki kesamaan dengan application layer pada model OSI. Protokol yang dicakup oleh lapisan ini diantara lainnya adalah HTTP, FTP, SMTP, DNS, dan lainnya.

2. Transport Layer 
Lapisan ini berguna untuk membuat komunikasi menggunakan connection session yang bersifat connection-oriented  atau broadcast. Dia berfungsi untuk memastikan bahwa setiap komunikasi dalam jaringan berjalan lancar. lapisan transport ini mengggunakan 2 protokol utama yaitu TCP dan UDP. Lapisan ini seperti layer transport pada OSI yang juga mengatur pembentukan segmen, dan juga pengaturan aliran.

3. Network Layer
Lapisan ini berfungsi untuk melakukan routingg/pemetaan serta memberikan setiap perangkat komputer identitas berupa IP address. Pemberian alamat IP ini berfungsi sebagia alamat yang berguna untuk menghubungkan beberapa perangkat dalam jaringan. Pada lapisan ini digunakan protokol berupa IP, ARP, ICMP, dan IGMP. Lapisan ini memiliki kesamaan dengan layer network pada model OSI yang sama-sama mengatur alamat jaringan dan routing.

4. Network Interface Layer
Lapisan ini berfungsi untuk menangani interaksi perangkat keras dan perangkat lunak dengan media transmisi fisik dan meletakkan frame jaringan yang adda di atas media jaringan yang digunakan. Teknologi transport yang dapat digunakan oleh TCP/IP banyak, mulai dari kabel listrik(tembaga), optik fiber, dan nirkabel. Lapisan ini memiliki kemiripan sifat dengan layer data link dan phisycal dalam model OSI yang mencakup pengiriman data dalam bentuk frame dan bit.
