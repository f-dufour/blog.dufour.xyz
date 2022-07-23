---
layout: default
title: Home
permalink: /all
---

{% for post in site.posts %}
  {% include list-post-short.html %}
{% endfor %}

<center>
<a href="/" class="cta">Hide older posts</a>
</center>