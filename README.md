# Jarkom-Modul-1-E22-2023

| Nama                       | NRP        |
| -------------------------- | ---------- |
| Anggara Saputra            | 5025211241 |
| Faizah Nurdianti Maghfirah | 5025211134 |

## Soal 1

**User melakukan berbagai perintah dengan menggunakan protokol FTP.**

Menampilkan Sequence Number (raw) & Acknowledgment Number (raw) - Request

![1](img/s.1.1.png)

Menampilkan Sequence Number (raw) & Acknowledgment Number (raw) - Response

![1](img/s.1.2.png)

Hasil Jawaban untuk 4 pertanyaan yang ada

![1](img/s.1.3.png)

## Soal 2

Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer

- Display filter `http contains "server"`

![image](https://github.com/fzhmghfrh/Jarkom-Modul-1-E22-2023/blob/main/img/s.2.1.png)

Jawab: gunicorn

![image](https://github.com/fzhmghfrh/Jarkom-Modul-1-E22-2023/blob/main/img/s.2.2.png)

## Soal 3

**A. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?** 

Ketika dilakukan filtering `ip.addr == 239.255.255.250 && udp.port == 3702` maka bisa langsung dihitung dan didapatkan hasilnya, yaitu **21**

![3](img/s.3.1.png)

**B. Protokol layer transport apa yang digunakan?**

Hasil filtering tadi juga akan menunjukan bahwa protokol yang digunakan adalah **UDP**

![3](img/s.3.2_8_9.png)

## Soal 4

Berapa nilai checksum yang didapat dari header pada paket nomor 130?
- Display filter `frame.number == 130` dan dilihat nilai checksumnya

![image](https://github.com/fzhmghfrh/Jarkom-Modul-1-E22-2023/blob/main/img/s.4.1.png)

Jawab: 0x18e5

![image](https://github.com/fzhmghfrh/Jarkom-Modul-1-E22-2023/blob/main/img/s.4.2.png)

## Soal 5

**Elshe menemukan suatu file packet capture yang menarik. Bantulah elshe untuk menganalisis file packet capture tersebut.**

Filtering dilakukan terlebih dahulu untuk mencari alamat login, agar dapat mengetahui password yang ditentukan dan akan dilakukan decode

![5](img/s.5.1.png)

**Berapa banyak packet yang berhasil di capture dari file pcap tersebut?**

File menunjukan **60** file pcap

![5](img/s.5.2.png)

**Port berapa pada server yang digunakan untuk service smtp?**

Detail menunjukan Source port adalah **25**

![5](img/s.5.3.png)

**Dari semua alamat ip yang tercapture, ip berapakah yang merupakan public ip?** 

IPv4 - 6 menunjukan 6 alamat ip dan hanya satu yang tidak local, yaitu **74.53.140.153**

![5](img/s.5.4.png)

![5](img/s.5.5.png)

## Soal 6

REVISI

- a1 e 5 u21 menunjukkan encoding yang digunakan yaitu a1z26 cipher
- server SOURCE ADDRESS 7812 is invalid menunjukkan nomor packet

![image](https://github.com/fzhmghfrh/Jarkom-Modul-1-E22-2023/blob/main/img/s.6.1.png)

- IP address packet 7812 yaitu 104.18.14.101 didecode

![image](https://github.com/fzhmghfrh/Jarkom-Modul-1-E22-2023/blob/main/img/s.6.2.png)

Jawab: JDRNJA

![image](https://github.com/fzhmghfrh/Jarkom-Modul-1-E22-2023/blob/main/img/s.6.3.png)

## Soal 7

**Berapa jumlah packet yang menuju IP 186.87.193.88?**

Filtering `ip.src == 184.87.193.88` menunjukan ada **6** packet

![7](img/s.7.1.png)

![7](img/s.7.2.png)

## Soal 8

**Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)**

`tcp.dst.port == 80 || udp.dstport == 80`

![8](img/s.3.2_8_9.png)

## Soal 9

**Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34**

`ip.src == 10.51.40.1 && ip.dst != 10.39.55.34`

![9](img/s.3.2_8_9.png)

## Soal 10

Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet
- Brute force dicari dari packet dengan protocol `TELNET`

![image](https://github.com/fzhmghfrh/Jarkom-Modul-1-E22-2023/blob/main/img/s.10.1.png)

Jawab: dhafin:kesayangannyak0k0

![image](https://github.com/fzhmghfrh/Jarkom-Modul-1-E22-2023/blob/main/img/s.10.3.png)

**REVISI**

Cara supaya tidak brute force: 
- Display filter frame contains "Login"
- Follow TCP stream

![image](https://github.com/fzhmghfrh/Jarkom-Modul-1-E22-2023/blob/main/img/s.10.2.png)


## Kendala

### Soal 9

Awalnya soal 9 tidak bisa mendapatkan hasil yang *benar* meskipun sudah memasukan kueri yang sama dengan yang saat ini

### Soal 5

Kesulitan dalam melakukan decode pada beberapa website
