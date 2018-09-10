---
layout: news_item
comments: true
title: "Cara Mengecilkan HTML di Blog Jekyll"
description: Cara Mengecilkan HTML di Blog Jekyll tanpa menggunakan plugin, compress html menggunakan javascript.
image: artikel-terkait-jekyll-page4.png
date: 2018-09-10 11:30:00 +0800
author: artipedia
categories: [widget,tutorial,blog]
---

## Mengapa kita harus mengecilkan HTML?
Kecepatan adalah faktor penting karena dapat meningkatkan peringkat di halaman pencarian Google. Meminimalkan HTML dapat menyebabkan peningkatan kecepatan sekitar 5% atau lebih. Situs web dapat lebih mudah dimuat bahkan pada koneksi yang lambat. Biasanya, file html terdiri dari banyak ruang kosong, komentar, baris baru, dll.

* TOC
{:toc}

## Bagaimana cara mengecilkan html?
Sejauh ini Anda dapat mengecilkan penggunaan html menggunakan Grunt atau Gulp, tetapi untuk pemula seperti saya akan sulit difahami, selain itu saya juga lebih suka solusi yang tidak melibatkan plugin.

### Langkah 1: Unduh file compress.html
Buka [tautan ini](https://github.com/penibelst/jekyll-compress-html/releases/download/v3.0.4/compress.html "File Compress HTML") dan unduh file compress.html.

### Langkah 2: Simpan file compress.html pada folder layout
Dalam repository anda cari folder `_layout` kemudian simpan file `compress.html` di folder tersebut.

### Langkah 3: Menambahkan front matter pada layout default
buka file `default.html` dalam folder `_layouts`. Copy kode di bawah kemudian simpan dibagian atas.

{% raw %}
```
---
layout: compress
---
```
{% endraw %}

isi dari file `default.html` akan tampak seperti di bawah ini

{% raw %}
```html
---
layout: compress
---

<!DOCTYPE html>
<html>
.
.
.

</html>
```
{% endraw %}

### Langkah 4: Simpan perubahan
Simpan dan _commit_ perubahannya. Secara default `compress.html` akan menjadi layout utama anda.

## Pengaturan Tambahan
jika Anda ingin opsi tambahan maka Anda dapat menggunakan kode dibawah dan simpan dalam file `_config.yml`.

```
compress_html:
    clippings: []
    comments: []
    endings: []
    ignore:
    envs: []
    blanklines: false
    profile: false
    startings: []
```

### Contoh 
Anda dapat mengunakan kode di bawah ini atau mempelajarinya sesuai dengan keinginan anda di [dokumentasi](http://jch.penibelst.de/ ).

```
compress_html:
  clippings: all
  comments: [""]
  endings: [html, head, body, li, dt, dd, rt, rp, optgroup, option, colgroup, caption, thead, tbody, tfoot, tr, td, th]
  profile: false
  blanklines: false
  ignore:
    envs: []
```
