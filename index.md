---
layout: default
title: Home
---
{% for post in site.posts %}
  <div id="post-short">
    <a href="{{site.url}}{{site.baseurl}}{{post.url}}">
      <h3>{{post.title}}</h3>
    </a>
    <i>posted on {{ post.date | date: "%-d %b %Y" }}</i>
    <p>
      {% if post.excerpt %}
        {{ post.excerpt }} ... read more
      {% else %}
        {{ post.content }}
      {% endif %}
    </p>
  </div>
{% endfor %}
