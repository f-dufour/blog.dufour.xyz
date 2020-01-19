---
layout: default
title: Categories
permalink: /categories/
---

<!-- TODO: Add the number of articles in each category-->

{% for category in site.categories %}
  - [{{category | first}}]({{site.url}}{{site.baseurl}}{{page.url}}{{category | first}})
{% endfor %}
