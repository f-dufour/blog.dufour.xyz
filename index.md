---
layout: default
title: Home
---

{% for post in site.posts %}
  <div id="post-short">
    <a href="{{site.url}}{{site.baseurl}}{{post.url}}">
      <h3>✹ {{post.title}}</h3>
    </a>
    <i>In {{ post.category.first }}, posted on {{ post.date | date: "%b, %-d %Y" }}</i>
    <p>
      {% if post.excerpt %}
        {{ post.excerpt | strip_html }} <a href="{{ post.url }}" class="cta">... read more</a>
      {% else %}
        {{ post.content }}
      {% endif %}
    </p>
  </div>
{% endfor %}
