---
title: PHENIX Gallery
abbrev: phenix_gallery
layout: default
weight: 2
---
# Gallery

{% assign images = site.data.gallery | sort: 'weight' %}
<ul class="photo-gallery">
  {% for image in images %}
    <li><img src="{{ image.path | relative_url }}" alt="{{ image.title}}" width="100px"/></li>
  {% endfor %}
</ul>
