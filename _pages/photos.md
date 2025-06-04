---
title: Photos
permalink: /photos/
---
{% include image-gallery.html %}

{% assign sorted_gallery = site.photo_gallery | sort: 'date' %}
<ul class="photo-gallery">
  <div class="img_row">
    {% for image in sorted_gallery reversed %}
      <figure>
        <a href="{{ image.image_path }}" class="image-popup" title="{{ image.title }} <br>{{ image.location }}. {{ image.month }} {{ image.year }}. Photo by {{ image.author }}." >
          <img src="//images.weserv.nl/?url={{ site.url | replace: 'http://','' }}{{ image.image_path | relative_url }}&w=300&h=300&output=jpg&q=50&t=square" alt="{{ image.alt }}" width="300" height="300">
        </a>
      </figure>
    {% endfor %}
    </div>
</ul>

