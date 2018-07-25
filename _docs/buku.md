---
title: Kumpulan Buku Referensi
description: Kumpulan buku referensi, buku elektronik sekolah, BSE, Buku Guru, Buku Siswa, Buku Administrasi, dll yang sangat berguna guna menunjang ilmu pengetahuan atau wawasan bagi para pembaca.
permalink: /buku/
redirect_from: /docs/buku/
---

Peribahasa mengatakan bahwa buku adalah jendela dunia. Diera digital ini beragam informasi dapat mudah didapatkan termasuk salah satunya Buku Elektronik yang sangat berguna guna menunjang ilmu pengetahuan atau wawasan bagi para pembaca.

Halaman ini berisi kumpulan buku elektronik (BSE) yang bisa anda unduh dan baca di blog ini.
<ol class="arti">{% for post in site.categories.buku %}
<li class="{% if page.title == post.title %}current{% endif %}">
<a href="{{ post.url }}">{{ post.title }}</a>
</li>
{% endfor %}
</ol>
