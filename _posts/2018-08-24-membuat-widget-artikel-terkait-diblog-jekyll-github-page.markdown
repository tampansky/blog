---
layout: news_item
comments: true
title: "Membuat Widget Artikel Terkait di Blog Jekyll"
description: Membuat Widget Artikel Terkait (related post) di Blog Jekyll (Github Pages) dengan langkah-langkah mudah.
image: artikel-terkait-jekyll-page4.png
date: "2018-18-24 20:48:09 -0500"
author: artipedia
categories: [widget,tutorial,blog]
---
* TOC
{:toc}

### Apa itu Widget Artikel Terkait
Widget Artikel Terkait (*related-post*) penting bagi sebuah blog. Kenapa? Karena salah satunya dapat menurunkan [bounce rate](https://en.wikipedia.org/wiki/Bounce_rate "Bounce Rate") blog, selain itu dapat mempermudah pengunjung dalam berselancar di blog.

Membuat artikel terkait pada blogspot dan wordpress mungkin anda semua sudah tahu bagaimana caranya. Akan tetapi widget artikel terkait yang akan buat disini adalah widget artikel terkait untuk blog jekyll (blog yang dihosting di Github).

### Cara membuat widget artikel terkait di blog Jekyll
Langkah-langkah membuatnya terdiri dari beberapa tahap:

#### Langkah Pertama : Membuat file `artikel-terkait.html`

![Membuat file baru]({{ "/img/artikel-terkait-jekyll-page.png"| absolute_url }} "Membuat file baru")

1. Cari folder bernama `_include` kemudian klik
2. Klik _create new file_
3. Beri nama file tersebut dengan `artikel-terkait.html`

![Menamai file]({{ "/img/artikel-terkait-jekyll-page.png2"| absolute_url }} "Menamai file")

4. Copy dan pastekan kedo dibawah ini dan simpan (commit)

{% raw %}
```liquid
<div class="recent no-print">
<h4><i class="fa fa-list" aria-hidden="true"></i>  Lihat lainnya</h4>
{% if page.path contains '_jekyll-themes' %}
 <div class="rect">
    {% for jekyll-themes in site.jekyll-themes  limit: 4 %}
         {% if jekyll-themes.url != page.url %}
             <a href="{{ jekyll-themes.url | prepend: site.baseurl }}">
                  <div class="rel">
                      <img alt="{{jekyll-themes.title | append:'jekyll theme'}}" src="/thumbs/{{ jekyll-themes.image }}">
                       <p><small>{{ jekyll-themes.title | truncate: 300 }}</small></p>
                  </div>
              </a>
        {% endif %}
    {% endfor %}
</div>
{% else %}
<div class="rect">
  {% assign maxRelated = 6 %}
  {% assign minCommonTags =  1 %}
  {% assign maxRelatedCounter = 0 %}
  {% for post in site.posts %}
    {% assign sameTagCount = 0 %}
    {% assign commonTags = '' %}
     {% for category in post.categories %}
      {% if post.url != page.url %}
        {% if page.categories contains category %}
          {% assign sameTagCount = sameTagCount | plus: 1 %}
          {% capture tagmarkup %} <span class="label label-default">{{ tag }}</span> {% endcapture %}
          {% assign commonTags = commonTags | append: tagmarkup %}
        {% endif %}
      {% endif %}
    {% endfor %}
    {% if sameTagCount >= minCommonTags %}
          <a href="{{ site.baseurl }}{{ post.url }}">
              <div class="rel">
                  <img alt="{{post.title}}" title="{{post.title}}" src="/img/{{post.image}}">
                     <p><small>{{ post.title | truncate: 300 }}</small></p>
              </div>
          </a>
      {% assign maxRelatedCounter = maxRelatedCounter | plus: 1 %}
      {% if maxRelatedCounter >= maxRelated %}
        {% break %}
      {% endif %}
    {% endif %}
  {% endfor %}
</div>
{% endif %}
 </div>
```
{% endraw %}

#### Langkah Kedua : Menambahkan kode `{% include recent.html %}`
1. Cari Folder `_layout` 
2. Cari dan buka file `post.html` (layout halaman posting)
3. Copy dan pastekan kode `{% include recent.html %}`. (letakan dibagian dimana anda inging meletakannya)
4. Simpan (commit)

#### Langkah Ketiga : Menambahkan `CSS`
Copy dan Pastekan Code CSS di bawah pada file css template anda!
```css
.recent {
  padding: 20px 40px 30px
}

.rel p {
  margin: 5px 0 0 0;
  line-height: 1em;
  font: bold 14px "poppins", sans-serif !important
}

.recent h4 {
  border-top: 1px solid #e8e8e8;
  border-bottom: 1px solid #e8e8e8;
  padding: 5px 0;
  font-size: 16px;
  margin: 0 0 15px 0
}

.rect {
  margin: 0 auto
}

.rel {
  width: 32.9%;
  display: inline-grid;
  padding: 5px;
  opacity: 0.8
}

.rel hover {
  opacity: 1
}

.desc img {
  width: 100%
}

.desc {
  margin-top: 30px
}

.rect a {
  color: #222
}

.rect a:hover {
  color: #fabc4c
}

@media (max-width: 568px) {
  article,
  .article-footer {
    margin: 0 !important
  }
  .recent {
    padding: 20px
  }
}

```





