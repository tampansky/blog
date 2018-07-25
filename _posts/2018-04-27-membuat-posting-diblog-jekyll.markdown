---
layout: news_item
comments: true
title: "Membuat Posting di Blog Jekyll / Github Pages"
description: Membuat posting di blog jekyll sangatlah mudah, anda hanya perlu membuat file postingan notepad, Atom, dll kemudian upload ke github di folder post.
date: "2018-02-19 20:48:09 -0500"
author: artipedia
categories: [Dasar, Tutorial]
---
* TOC
{:toc}
### Membuat Posting di Blog Jekyll
Salah satu hal terbaik dalam blog Jekyll adalah Anda dapat mempublikasikan dan mengelola blog hanya dengan mengelola folder file teks di komputer Anda atau secara langsung di Github. 

Untuk membuat posting baru, yang perlu Anda lakukan adalah membuat file di `_posts` direktori. File tersebut dapat dibuat di Github secara langsung, ataupun menggunakan Aplikasi yang biasa anda gunakan, seperti notepad, Atom, dll. 

### Memberi Nama File
Perlu dicatat file posting yang anda buat harus diberi nama sesuai dengan format berikut:
```
YEAR-MONTH-DAY-title.MARKUP
```
1. YEAR   : diisi dengan tahun (empat angka)
2. MONTH  : diisi dengan bulan (dua angka)
3. Day    : diisi dengan tanggal (dua angka)
4. Title  : diisi dengan judul posting
5. Markup : diisi dengan .md atau .markdown (Merupakan ekstensi file yang mewakili format yang digunakan dalam file)

Berikut ini adalah contoh dari nama file postingan yang valid:
```
2018-04-31-membuat-posting-diblog.md
2018-04-31-membuat-posting-diblog.markdown
```

### Format Penulisan Posting

```yaml
---
layout: post
title: "Judul Artikel"
date: "2018-02-19"
author: artipedia
categories: [referensi]
---

## SubJudul
lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum 
lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum 
lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum
lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum 
 lorem ipsum lorem ipsum lorem ipsum.

lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum 
lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum 
lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum
lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum 
 lorem ipsum lorem ipsum lorem ipsum.


```


### Keterangan :
1. title : "Isi dengan Judul Artikel Anda".
2. date : "Isi dengan tanggal dengan format Tahun-bulan-tanggal".
3. author : "Isi dengan username github anda".
4. categories: "isi dengan kategori artikel".

## Format Penulisan 

### Paragraf
Paragraf ditulis dan dipisahkan dengan enter

### Header
Penulisan sub judul 

{% raw %}
```liquid
# Judul <h1> tag
## Sub Judul <h2> tag
### Sub Judul <h3> tag
#### Sub Judul <h4> tag
##### Sub Judul <h5> tag
###### This is an <h6> tag
```
{% endraw %}

Hasilnya
# Judul h1 
## Sub Judul h2 
### Sub Judul h3 
#### Sub Judul h4 
##### Sub Judul h5 
###### Sub Judul h6

## Bold
Menebalkan huruf terdapat dua cara
```
1. **Contoh**
2. __Contoh__.
```
Hasilnya
**Contoh**

## Italic
```
1. *Contoh*
2. _Contoh_.
```
Hasilnya
*Contoh*

## Link
Untuk menyisipkan link
```
1. [ArtiPedia](http://artipedia.site/)
2. [ArtiPedia](http://artipedia.site/ "Link dengan Atribut Title")
```
Hasilnya 
1. [ArtiPedia](http://artipedia.site/)
2. [ArtiPedia](http://artipedia.site/ "Link dengan Atribut Title")

## Image
```
1. Inline-style: 
![alt text](https://artipedia.site/img/logo-2x.png "Logo Title Text 1")

2. Reference-style: 
![alt text][logo]
[logo]: https://artipedia.site/img/logo-2x.png "Logo Title Text 2"
```

Hasilnya
1. Inline-style: 

![alt text](https://artipedia.site/img/logo-2x.png "Logo Title Text 1")

2. Reference-style: 

![alt text][logo]

[logo]: https://artipedia.site/img/logo-2x.png "Logo Title Text 2"

## Blockquote
Untuk menambahkan <code>blockquote</code> tambahkan <code>></code> sebelum/pada awal paragraf
```
> Tes penulisan blockquote
```
Hasilnya
> Tes penulisan blockquote
