<!-- ---
layout: single-portfolio
title: "Projects"
permalink: /projects/
author_profile: true
header:
  og_image: "projects/ecdf.png"
entries_layout: grid
sort_order: forward
---

My research focuses on ... 

<nbsp>

<!-- {% include base_path %} -->

<!-- {% assign ordered_pages = site.projects | sort:"order_number" %}

{% for post in ordered_pages %}
  {% include archive-single.html type="grid" %}
{% endfor %} --> -->

---
layout: archive-taxonomy
title: "Research projects"
subtitle: "Research project subtitle"
permalink: /projects/
author_profile: true
header:
  og_image: "projects/ecdf.png"
classes: wide
---

{% include base_path %}

{% for post in site.projects reversed %}
  {% include archive-single.html %}
  {% if page.subtitle %}{{ page.subtitle }}{% endif %}
{% endfor %}