---
title: Photos
permalink: /photos/
---

{% assign sorted_gallery = site.photo_gallery | sort: 'date' %}
<ul class="photo-gallery">
  <div class="img_row">
    {% for image in sorted_gallery reversed %}
      <figure>
        <a href="{{ image.image_path }}" class="image-popup" title="{{ image.title }} 
                                                                    <br>{{ image.location }}. {{ image.month }} {{ image.year }}. Photo by {{ image.author }}.">
          <img src="{{ image.image_path }}" alt="{{ image.alt }}" style="width:{{ image.width }}">
        </a>
      </figure>
    {% endfor %}
    </div>
</ul>