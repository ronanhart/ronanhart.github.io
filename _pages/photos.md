---
title: Photos
permalink: /photos/
author_profile: false
---
{% assign sorted_gallery = site.photo_gallery | sort: 'date' %}

  {% if sorted_gallery.size == 2 %}
    {% assign gallery_layout = 'half' %}
  {% elsif sorted_gallery.size >= 3 %}
    {% assign gallery_layout = 'third' %}
  {% else %}
    {% assign gallery_layout = '' %}
  {% endif %}

<figure class="{{ gallery_layout }}">
  {% for image in sorted_gallery reversed %}
    <a href="{{ image.image_path }}" class="image-popup" title="{{ image.title }} <br>{{ image.location }}. {{ image.month }} {{ image.year }}. Photo by {{ image.author }}." width="100px">
      <img src="{{ image.image_path }}" alt="{{ image.alt }}" width="100px">
    </a>
  {% endfor %}
</figure>
<!-- a comment 
more comments
-->
