---
title: Membuat Blog Jekyll Secara Lokal
description: Membuat jekyll blog secara lokal di komputer anda, mengedit blog Jekyll secara lokal, membuat perubahan dan melihat bagaimana perenderannya di browser.
permalink: /docs/membuat-blog-jekyll-secara-lokal/
---

Jika Anda sudah memiliki Ruby dan RubyGems ([lihat cara instal Ruby](https://blog.artipedia.site/id/cara-install-ruby.html)) diinstal di PC anda,  Anda dapat membuat situs Jekyll baru dengan melakukan hal berikut menggunakan command prompt:


```sh
# Install Jekyll and Bundler gems 
gem install jekyll bundler

# membuat jekyll blog contoh ./myblog dengan 
jekyll new myblog

# menuju directory folder jekyll blog
cd myblog

# membangun situs di server lokal
bundle exec jekyll serve

# sekarang buka http://localhost:4000 dibrowser anda
```



