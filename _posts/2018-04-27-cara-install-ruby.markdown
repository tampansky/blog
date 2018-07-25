---
layout: news_item
title: Instal Ruby dan Ruby DevKit
date: "2018-02-20 20:48:09 -0500"
categories: [Dasar, Tutorial,]
description: Ruby adalah bahasa pemrograman yang ditulis Jekyll. Anda harus menginstal Ruby dan DevKit yang sesuai, yang diperlukan untuk membangun beberapa dependensi Jekyll sebagai "ekstensi asli.
author: artipedia
comments: true
---
* TOC
{:toc}

Ruby adalah bahasa pemrograman yang ditulis Jekyll. Anda harus menginstal Ruby dan DevKit yang sesuai, yang diperlukan untuk membangun beberapa dependensi Jekyll.

### Instal Ruby
Pertama, klik tombol di bawah dan unduh penginstal untuk Ruby v2.0.0 yang sesuai dengan arsitektur sistem Anda (x86 / x64).

[RubyInstaller Downloads][RubyInstaller-downloads] 

Jalankan installer dan ikuti langkah-langkah instalasi. Saat Anda masuk ke layar di bawah, pastikan untuk mencentang kotak “Tambah Ruby yang dapat dieksekusi ke PATH” Anda.

![Centang Ruby Path]({{ "/img/ruby-path.png"| absolute_url }})

Klik Pasang dan Ruby akan dipasang dalam hitungan detik.

### Update
Ruby installer Versi terbaru Ruby+Devkit 2.4.4-1 (x64) sehingga anda tidak perlu mengikuti langkah-langkah yang tertera di bawah.

### Instal Ruby DevKit
Jekyll memiliki beberapa dependensi yang hanya menyediakan kode sumber mentah. Untuk membuatnya menjadi executable yang berfungsi penuh, Anda mungkin perlu menginstal Kit Pengembangan.

Klik tombol di bawah dan unduh arsip DevKit yang sesuai dengan instalasi Ruby dan arsitektur sistem Anda. Untuk Ruby v2.0.0, nama file akan dimulai dengan DevKit-mingw64. Pilih versi 32bits atau 64bits tergantung pada sistem Anda.

[RubyInstaller Downloads][RubyInstaller-downloads]

Unduhan dan ekstrak file di folder C: contoh C:\RubyDevKit\. Klik Extract dan tunggu hingga proses selesai.

Selanjutnya, Anda perlu menginisialisasi DevKit dan mengikatnya ke instalasi Ruby Anda. Buka command prompt seperti gambar di bawah ini.

![Menjalankan Command Prompt]({{ "/img/cmd.png"| absolute_url }})

{% raw %}
```
cd C:\RubyDevKit
```
{% endraw %}

Langkah selanjutnya ketikkan:.

{% raw %}
```
ruby dk.rb init
```
{% endraw %}

Instal DevKit, kombinasikan dengan instalasi Ruby Anda.
{% raw %}
```
ruby dk.rb install
```
{% endraw %}

Ringkasan
Anda sekarang memiliki instalasi Ruby yang berfungsi pada mesin Anda dan Anda dapat membuat aplikasi yang berfungsi penuh menggunakan Ruby Development Kit. Ruby menyertakan cara untuk menginstal apa yang disebut gems—software perangkat lunak yang dapat Anda gunakan dari baris perintah yang sangat diperlukan untuk membangun blog Jekyll.

[RubyInstaller]: https://rubyinstaller.org/
[RubyInstaller-downloads]: https://rubyinstaller.org/downloads/
