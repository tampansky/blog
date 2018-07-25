---
layout: news_item
comments: true
title: "Cara Mengaktifkan Fitur HTTPS Gratis di Github"
description: Cara setting (mengaktifkan) fitur HTTPS gratis bagi custom domain di Github Pages. Mengatasi unavailable for your site because a certificate has not yet been issued for your domain di Github Pages.
date: "2018-06-04 12:48:09 "
image: fiturhttpsgithub.png
author: artipedia
categories: [Dasar, Tutorial]
---
* TOC
{:toc}

[Github Pages](https://pages.github.com/) saat ini menurut saya menjadi alternatif terbaik untuk mempublikasikan situs web yang indah, ringan, loading cepat. . GitHub Pages telah mendukung domain khusus sejak 2009, serta mendukung HTTPS sejak 2016 . 

Pada 01 Mei 2018 lalu Github Pages memberikan fitur gratis terbaru yaitu fitur HTTPS yang mendukung Custom Domain.

### Apa itu HTTPS?
HTTPS (paling dikenal sebagai ikon kunci di bilah kiri alamat browser Anda) yang dapat mengenkripsi lalu lintas antara server GitHub dan browser.

*Hypertext Transfer Protocol Secure* atau biasa kita sebut dengan **HTTPS** adalah sebuah protocol komunikasi dalam jaringan komputer yang aman karena HTTPS membuat perintah atau data yang melalui protocol HTTPS inidilindungi dengan sistem encryp melalui berbagi format sehingga dengan demikian akan menyulitkan para hacker yang berusaha membajak isi dokumen yang dikirimkan.

HTTPS adalah gabungan dari protocol HTTP dengan SSL/TSL protokol. Seluruh komunikasi yang dilakukan melalui HTTPS akan dienkripsi dan dianalisa dengan tujuan untuk keamanan ketika terjadi transaksi data melalui internet.

Melalui fitur ini, situs web anda yang dihosting di Github dapat diases melalui HTTPS, sehingga lebih seo friendly dan meyakinkan pembaca kalau situs anda situs yang aman.

### Konfigurasi HTTPS Custom Domain

Perbarui DNS domain anda dengan alamat IP baru.
1. 185.199.108.153
2. 185.199.109.153
3. 185.199.110.153
3. 185.199.111.153

Setelah data DNS diperbarui tunggu hingga DNS terupdate oleh provider, umumnya tidak kurang dari 24 Jam tergantung provider mana yang anda gunakan (tempat beli domain anda).

Langkah selanjutnya di akun github pada halaman repository anda hapus domain kemudian simpan, dan tambahkan kembali domain tersebut.

![Menamai Repositori]({{ "/img/enforcehttpsfixed.png"| absolute_url }})

Apabila **Enforce HTTPS** tidak bisa diceklis seperti gambar di atas, anda hanya tinggal menunggu karena prosesnya memakan maktu maksimal 24 jam sampai tersedia.

### Manfaat Mengaktifkan Fitur HTTPS di Github 
1. Waktu pemuatan situs lebih cepat
2. Alamat IP baru ini tidak hanya memungkinkan kami untuk melayani situs Anda melalui HTTPS, tetapi juga menempatkan situs Anda di belakang jaringan pengiriman konten (CDN) , memungkinkan kami untuk melayani situs Anda dari pusat data di seluruh dunia dengan kecepatan cepat, dan menawarkan tambahan perlindungan terhadap serangan DDoS . Meskipun alamat IP sebelumnya akan tetap tersedia untuk periode transisi, sebaiknya Anda bermigrasi ke alamat IP baru untuk mendapatkan manfaat ini.

