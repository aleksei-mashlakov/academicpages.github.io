---
layout: archive
title: "Posts"
permalink: /posts/
author_profile: true
teaser: /images/500x300.png
header:
  og_image: "posts/ecdf.png"
sort_by: date
entries_layout: grid
sort_order: forward
---

My posts are about ... 

<nbsp>

<!-- {% include base_path %} -->

{% assign ordered_pages = site.posts | sort:"order_number" %}

{% for post in ordered_pages %}
  {% include archive-single.html type="grid" %}
{% endfor %}