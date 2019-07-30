---
layout: news_item
comments: true
title: "Memasang Animasi Background Partikel di Blog"
description: Memasang Animasi Background Partikel di Blog, Background animasi partikel dengan menggunakan javascript particle.js.
date: "2018-06-17 12:48:09 "
image: partikelbackground.png
author: artipedia
categories: [Dasar, Tutorial]
---
* TOC
{:toc}

## Perkenalan
Pernahkan anda melihat blog/web dengan background berupa partikel-partikel yang bergerak, seperti contoh di bawah? Kali ini saya akan membagikan cara memasang background partikel di blog/web.

Contoh web/blog yang menggunakan background particle.js
1. https://elivecoin.com
2. https://swopcrypto.com
3. https://livecointrackers.com

Background di atas merupakan background dengan menggunakan particle.js. Particles.js adalah Javascript Library yang ringan untuk membuat partikel yang dapat membuat halaman blog/web anda tampak cantik.

## Pemasangan
Langkah 1: Buka situs web [particle.js](https://vincentgarreau.com/particles.js "Particle.js"). di Situs web tersebut anda dapat melihat demo serta membuat dan mendownload pengaturan yang akan digunakan di blog/web anda.

Langkah 2: Unduh Partikel.js (anda bisa mengunduhnya di github atau langsung).

Langkah 3: Setelah diunduh, extrak file tersebut kemudian cari file yang bernama particles.js atau particles.min.js. Salin file tersebut  kemudian unggah ke server sendiri atau bisa juga menggunakan server gratis.

<p class="note info">Langkah 2 dan 3 bisa di lewati apabila anda tidak memiliki server pribadi (hosting)</p>

Langkah 4: Menambahkan script partcle.js sebelum tag `</head>` pada html anda
```
.....
<script src="//cdn.jsdelivr.net/particles.js/2.0.0/particles.min.js"></script>
</head>
```


Langkah 5: Menambahkan elemen `<div id="particles-js"></div>` pada html. Contoh yang saya gunakan, dengan menyimpannya tepat di bawah `<body>`.
```html
<body>
<div id="particles-js"></div>
<header>
...........

```
Langkah 6: Menambahkan script json di bawah ini di atas tag </body>
```
<script type="text/javascript">
 particlesJS("particles-js", Tambahkan kode json yang anda unduh disini);
</script>
```
atau anda bisa menggunakan kode di bawah ini
```
<script type="text/javascript">
 particlesJS("particles-js",{
 "particles": {
 "number": {
 "value": 80,
 "density": {
 "enable": true,
 "value_area": 800
 }
 },
 "color": {
 "value": "#ffffff"
 },
 "shape": {
 "type": "circle",
 "stroke": {
 "width": 0,
 "color": "#000000"
 },
 "polygon": {
 "nb_sides": 5
 },
 "image": {
 "src": "img/github.svg",
 "width": 100,
 "height": 100
 }
 },
 "opacity": {
 "value": 0.5,
 "random": false,
 "anim": {
 "enable": false,
 "speed": 1,
 "opacity_min": 0.1,
 "sync": false
 }
 },
 "size": {
 "value": 3,
 "random": true,
 "anim": {
 "enable": false,
 "speed": 40,
 "size_min": 0.1,
 "sync": false
 }
 },
 "line_linked": {
 "enable": true,
 "distance": 150,
 "color": "#ffffff",
 "opacity": 0.4,
 "width": 1
 },
 "move": {
 "enable": true,
 "speed": 6,
 "direction": "none",
 "random": false,
 "straight": false,
 "out_mode": "out",
 "bounce": false,
 "attract": {
 "enable": false,
 "rotateX": 600,
 "rotateY": 1200
 }
 }
 },
 "interactivity": {
 "detect_on": "canvas",
 "events": {
 "onhover": {
 "enable": true,
 "mode": "repulse"
 },
 "onclick": {
 "enable": true,
 "mode": "push"
 },
 "resize": true
 },
 "modes": {
 "grab": {
 "distance": 400,
 "line_linked": {
 "opacity": 1
 }
 },
 "bubble": {
 "distance": 400,
 "size": 40,
 "duration": 2,
 "opacity": 8,
 "speed": 3
 },
 "repulse": {
 "distance": 200,
 "duration": 0.4
 },
 "push": {
 "particles_nb": 4
 },
 "remove": {
 "particles_nb": 2
 }
 }
 },
 "retina_detect": true
});
</script>
```

## Opsi Pengaturan lainnya
SALAH INI GOBLOK


