# Jarkom-Modul-1-E22-2023

| Nama                       | NRP        |
| -------------------------- | ---------- |
| Anggara Saputra            | 5025211241 |
| Faizah Nurdianti Maghfirah | 5025211222 |

## Soal 1

**User melakukan berbagai perintah dengan menggunakan protokol FTP.**

Menampilkan Sequence Number (raw) & Acknowledgment Number (raw) - Request

gambar

Menampilkan Sequence Number (raw) & Acknowledgment Number (raw) - Response

gambar

Hasil Jawaban untuk 4 pertanyaan yang ada

gambar

## Soal 2

## Soal 3

**A. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?** 

Ketika dilakukan filtering `ip.addr == 239.255.255.250 && udp.port == 3702` maka bisa langsung dihitung dan didapatkan hasilnya, yaitu **21**

gambar

**B. Protokol layer transport apa yang digunakan?**

Hasil filtering tadi juga akan menunjukan bahwa protokol yang digunakan adalah **UDP**

gambar

## Soal 4

## Soal 5

**Elshe menemukan suatu file packet capture yang menarik. Bantulah elshe untuk menganalisis file packet capture tersebut.**

Filtering dilakukan terlebih dahulu untuk mencari alamat login, agar dapat mengetahui password yang ditentukan dan akan dilakukan decode

gambar

**Berapa banyak packet yang berhasil di capture dari file pcap tersebut?**

File menunjukan **60** file pcap

gambar

**Port berapa pada server yang digunakan untuk service smtp?**

Detail menunjukan Source port adalah **25**

gambar

**Dari semua alamat ip yang tercapture, ip berapakah yang merupakan public ip?** 

IPv4 - 6 menunjukan 6 alamat ip dan hanya satu yang tidak local, yaitu **74.53.140.153**

gambar

gambar

## Soal 6

## Soal 7

**Berapa jumlah packet yang menuju IP 186.87.193.88?**

Filtering `ip.src == 184.87.193.88` menunjukan ada **6** packet

gambar

gambar

## Soal 8

**Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)**

`tcp.dst.port == 80 || udp.dstport == 80`

gambar

## Soal 9

**Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34**

`ip.src == 10.51.40.1 && ip.dst != 10.39.55.34`

gambar

## Soal 10

## Kendala

### Soal 9

Awalnya soal 9 tidak bisa mendapatkan hasil yang *benar* meskipun sudah memasukan kueri yang sama dengan yang saat ini

### Soal 5

Kesulitan dalam melakukan decode pada beberapa website
