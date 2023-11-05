# PING, IP ROUTE, LOGICAL AND PHYSICAL ROUTER MODEL

## Ping antar PC
Melakukan ping antar PC yang terhubung pada satu router yang sama melalui kabel ethernet.
<p align="center">
<img src="../assets/winbox-ping-1.jpeg">
<br>
<i>Gambar: Hasil ping pada PC dalam satu jaringan.</i>
</p>

<p align="center">
<img src="../assets/winbox-ping-2.jpeg">
<br>
<i>Gambar: Hasil ping pada PC dalam satu jaringan.</i>
</p>

<p align="center">
<img src="../assets/winbox-ping3.jpeg">
<br>
<i>Gambar: Hasil ping pada PC dalam satu jaringan.</i>
</p>

## Physical Model


## Logical Model
<p align="center">
<img src="../assets/logical-model-routers.jpg">
<br>
<i>Gambar: Logical model topologi semua router</i>
</p>

<p align="center">
<img src="../assets/logical-model-pcs.jpg">
<br>
<i>Gambar: Logical model yang mengilustrasikan cara</i>
</p>


## Print IP Route
Menampilkan IP route pada raouter menggunakan winbox.

<p align="center">
<img src="../assets/winbox-print-route.jpeg">
<br>
<i>Gambar: Hasil print IP route</i>
</p>

Pada gambar diatas dapat dilihat rute yang sudah dikonfigurasi pada router melalui aplikasi winbox. Pada gambar diatas, terlihat bahwa sudah dikonfigurasikan rute untuk ether1 saja, dan belum dikonfigurasikan untuk ether yang lainnya. 

Pada saat menggunakan command ip route print pada terminal winbox, terdapat keterengan Flags yang muncul sebagai status dari routing yang ada, diantaranya dalah:
- X: disabled
- A: active
- D: dynamic
- C: connect
- S: static
- r: rip
- b: bgp
- o: ospf
- m: mme
- B: blackhole
- U: unreachable
- P: prohibit

Dapat dilihat bahwa kedua rute yang sudah terkonfigurasi memiliki status **ADC** yang berarti kedua rute tersebut available, bersifat dynamic, dan terhubung.