---
layout: news_item
comments: true
title: "Cara Membuat Tombol Social Share di Blog Jekyll"
description: Cara Membuat / Memasang Tombol Social Share di Blog Jekyll dengan mudah tanpa javascript bagi pemula.
date: "2018-02-27 20:48:09 -0500"
image: sosial-share.png
author: artipedia
categories: [Dasar, Tutorial]
---
* TOC
{:toc}

## Mengapa tombol sosial share sangat penting

Jika Anda membaca banyak melalui internet, maka Anda tahu betapa sulitnya berbagi artikel dengan teman Anda jika website yang anda kunjungi tidak memiliki tombol sosial share. Sehingga dengan terpaksa anda harus menyalinnya secara manual, membuka akun email Anda, dan mengetikan setiap detail lalu mengirimnya.

## Bagaimana Cara Membuat Tombol Social Share?

1. Buat file baru di folder `_include` berinama file dengan

`social-buttons.html`

2. Isikan kode di bawah ini kemudian simpan.

`
<div class="social-buttons">
<a href="https://facebook.com/sharer.php?u={{ site.url }}{{ page.url }}" rel="nofollow" target="_blank" title="Share on Facebook" class="z-2 z-h social fb" onclick="window.open(this.href, 'mywin', 'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;"><i class="fa fa-facebook-square fa-2x" aria-hidden="true"></i></a>
<a href="https://twitter.com/intent/tweet?text={{ page.title }}&url={{ site.url }}{{ page.url }}&via=bootyocean18" rel="nofollow" target="_blank" title="Share on Twitter" class="z-2 z-h social tw" onclick="window.open(this.href, 'mywin','left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;"><i class="fa fa-twitter-square fa-2x" aria-hidden="true"></i></a>
<a href="https://plus.google.com/share?url={{ site.url }}{{ page.url }}" rel="nofollow" target="_blank" title="Share on Google+" class="z-2 z-h social gp" onclick="window.open(this.href, 'mywin','left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;"><i class="fa fa-google-plus-square fa-2x" aria-hidden="true"></i></a>
<a href="http://www.linkedin.com/shareArticle?mini=true&url={{ site.url }}{{ page.url }}&title={{ page.title }}&summary={{ page.summary }}&source={{ site.url }}" rel="nofollow" target="_blank" title="Share On LinkedIn" class="z-2 z-h social li" onclick="window.open(this.href, 'mywin','left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;"><i class="fa fa-linkedin-square fa-2x" aria-hidden="true"></i></a>
<a href="http://www.reddit.com/submit?url={{ site.url }}{{ page.url }}&title={{ page.title }}" rel="nofollow" target="_blank" title="Share On Reddit" class="z-2 z-h social rd" onclick="window.open(this.href, 'mywin','left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;"><i class="fa fa-reddit-square fa-2x" aria-hidden="true"></i></a>
<a href="http://www.stumbleupon.com/submit?url={{ site.url }}{{ page.url }}&title={{ page.title }}" rel="nofollow" target="_blank" title="Stumble This Page" class="z-2 z-h social su" onclick="window.open(this.href, 'mywin','left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;"><i class="fa fa-stumbleupon-circle fa-2x" aria-hidden="true"></i></a>
</div>

`


3. Cari folder `_sass` kemudian buat file baru
4. Berinama file tersebut dengan  nama `_social-buttons.scss`
5. Copy Code CSS di bawah ini kemudian pastekan didalamnya
6. Simpan


`css
.social-buttons {
  text-align: center;
  margin: 2em 1em;

  h3 {
    text-align: left;
  }

  .social {
    margin: 5px;}

  .fb {
   color:  #3b5998;
     &:hover{color: #222}
  }

  .tw {
color: #1da1f2;
    &:hover{color: #222}
  }
  .gp {
color: #dd4b39;
    &:hover{color: #222}
  }
  .li {
color: #0077b5;
 &:hover{color: #222}  }
  .rd {
color: #ff4500;
 &:hover{color: #222}
  }
  .su {
color: #eb4924;
 &:hover{color: #222}
  }
}

`


7. Cari folder css kemudian buka file <code>screen.scss</code>  tambahkan kode  <code>@import "social-buttons";</code> di bagian paling bawah kemudian simpan.

8. Cari folder <code>_layout</code> kemudian buka file dengan <code>posts.html</code> (layout halaman posting blog anda) nama file sesuai dengan template anda.

9. Tempatkan kode di bawah ini 

`
{% include social-buttons.html %}
`


Dibagian dimana pun Anda ingin tombol sosial share muncul.

