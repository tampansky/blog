---
title: Daftar Isi
description: Halaman ini berisi kumpulan arsip / daftar isi dari ArtiPedia. Anda juga bisa berkontribusi dengan menulis artikel di ArtiPedia.
permalink: /docs/daftar-isi/
---

<h4><a href="https://artipedia.site/docs/administrasi" title="Kumpulan Administrasi">Administrasi</a></h4>
<ol class="arti">
{% for post in site.categories.administrasi %}
<li class="{% if page.title == post.title %}current{% endif %}">
<a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
</li>  {% endfor %}
</ol>
<h4><a href="https://artipedia.site/docs/berita/" title="Kumpulan Berita">Berita</a></h4>
<ol class="arti">
{% for post in site.categories.berita %}
<li class="{% if page.title == post.title %}current{% endif %}">
<a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
</li>  {% endfor %}
</ol>
<h4><a href="https://artipedia.site/docs/buku/" title="Kumpulan Buku">Buku</a></h4>
<ol class="arti">
{% for post in site.categories.buku %}
<li class="{% if page.title == post.title %}current{% endif %}">
<a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
</li>
{% endfor %}
</ol>
 <h4><a href="https://artipedia.site/docs/referensi/" title="Kumpulan Berita">Referensi</a></h4>
<ol class="arti">
{% for post in site.categories.referensi %}
<li class="{% if page.title == post.title %}current{% endif %}">
<a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
</li>  {% endfor %}
</ol>
  <h4><a href="https://artipedia.site/docs/rpp" title="Kumpulan RPP">RPP</a></h4>
<ol class="arti">
{% for post in site.categories.rpp %}
<li class="{% if page.title == post.title %}current{% endif %}">
<a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
</li>  {% endfor %}
</ol>

