---
layout: default
title: Categories
permalink: /categories
---

<!-- TODO: Add the number of articles in each category-->

{% for category in site.categories %}

  - [{{category | first}}]({{site.url}}{{page.url}}{{category | first}})

{% endfor %}
