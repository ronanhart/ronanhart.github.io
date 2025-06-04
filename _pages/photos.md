---
title: Photos
permalink: /photos/
---

{% assign sorted_gallery = site.photo_gallery | sort: 'date' reversed %}
<ul class="photo-gallery">
  <div class="img_row">
    {% for image in sorted_gallery %}
      <figure>
        <a href="{{ image.image_path }}" class="image-popup" title="{{ image.title }}. Photo by {{ image.author }}. {{ image.location }}. {{ image.month }} {{ image.year }}">
          <img class="col one" src="{{ image.image_path }}" alt="{{ image.alt }}" style="width:{{ image.width }}">
        </a>
      </figure>
    {% endfor %}
    </div>
</ul>