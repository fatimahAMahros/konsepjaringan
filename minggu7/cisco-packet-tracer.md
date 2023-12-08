`Tugas ini merupakan tugas mata kuliah konsep jaringan  yang di bimbing oleh Bpk. Ferry Astika S`

## Cisco Packet Tracer

Cisco Packet Tracer adalah software simulasi jaringan yang dikembangkan oleh Cisco System. Software ini dirancang untuk membantu dalam pemahaman, perancangan, dan pengujian konsep jaringan komputer yang berbeda dalam sebuah lingkungan virtual yang aman. Packet Tracer ini menjadi alat yang sangat berguna dalam pendidikan, pelatihan, perencanaan jaringan, dan pengembangan keterampilan jaringan. 

### Membuat Topologi Jaringan dan Mengirimkan Packet antar Device

Sekarang, kita akan membuat model topologi jaringan menggunakan cisco yang memiliki 2 router, 2 switch, dan 4 PC seperti contoh di bawah.
<p align="center">
<img src="../assets/desain-target.jpg">
</p>

1. Pertama, kita pasang 2 router tipe 1841, 2 switch tipe 2960-24, dan 4 buah PC tipe PC-PT. Komponen-komponen ini akan secara otomatis diberi nama sesuai dnegan urutan pembuatannya.
<p align="center">
<img src="../assets/cisco-components.png">
</p>

2. Hubungkan kedua router menggunakan kabel *copper cross-over* dan pilih opsi fastEthernet 0/1 pada keduanya.
<p align="center">
<img src="../assets/cisco-crosscable.png">
</p>

3. Hubungkan router0(fastEthernet 0/0) dengan switch0(fastEthernet 0/1) menggunakan *copper straight*. Kemudian hubungkan switch0(fastEthernet 0/2) dengan PC0(fastEthernet 0) menggunakan kabel *copper straight* dan hubungkan  switch0(fastEthernet 0/3) dengan PC2(fastEthernet 0) menggunakan kabel yang sama.
<p align="center">
<img src="../assets/cisco-straightcable.png">
</p>

4. Konfigurasikan router0 pada bagian interface>fastEthernet 0/0 dan interface>fastEthernet 0/1 untuk mengatur IP dari router. Kemudian atur juga bagian Routing>RIP, RIP ini memungkinkan agar nantinya dapat dilakukan komunikasi antara PC dengan router yang berbeda. Jangan lupa untuk mengatur port status pada fastEthernet 0/0 dan fast ethernet 0/1 sehingga dalam kondisi On.
<p align="center">
<img src="../assets/router0-fe00.png">
<img src="../assets/router0-fe01.png">
<img src="../assets/router0-rip.png">
</p>

5. Setelah itu, kita konfigurasi router1 seperti yang dilakukan pada router0 yakni pada bagian interface>fastEthernet 0/0 dan interface>fastEthernet 0/1 untuk mengatur IP dari router serta pada routing>RIP. Jangan lupa untuk mengatur port status pada fastEthernet 0/0 dan fast ethernet 0/1 sehingga dalam kondisi On.
<p align="center">
<img src="../assets/router1-fe00.png">
<img src="../assets/router1-fe01.png">
<img src="../assets/router1-rip.png">
</p>

6. Setelah itu kita konfigurasikan IP dari setiap PC yakni pada bagian interface>fastEthernet0 dan menjadikan port statusnya menyala/On.
<p align="center">
<img src="../assets/pc0-fe0.png">
<img src="../assets/pc2-fe0.png">
<img src="../assets/pc1-fe0.png">
<img src="../assets/pc3-fe0.png">
</p>

7. Kemudian, kita konfigurasikan pula pada global>settings sehingga Default Gateway-nya sesuai dengan IP fastEthernet 0/0 dari router mereka. Hal ini agar antar PC yang berbeda router juga dapat berkomunikasi.
<p align="center">
<img src="../assets/pc0-defgate.png">
<img src="../assets/pc2-defgate.png">
<img src="../assets/pc1-defgate.png">
<img src="../assets/pc3-defgate.png">
</p>

8. Jalankan command ping pada salah satu PC dan lakukan ping terhadap PC lain yang memiliki router yang sama dan PC yang memiliki router yang berbeda. Di sini kita mengggunakan PC0 untuk melakukan ping. Buka tab Desktop pada PC0 dan buka command prompt. Kita lakukan ping pada PC2(IP=192.168.1.20, router yang sama) kemudian ping pada PC1(IP=192.168.2.10, router yang berbeda). Dapat kita lihat bahwa PC0 sudah dapat melakukan ping pada PC lainnya, baik yang memiliki router yang sama maupun yang memiliki router yang berbeda.
<p align="center">
<img src="../assets/pc0-ping.png">
</p>