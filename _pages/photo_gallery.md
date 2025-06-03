---
title: Photos
permalink: /photo_gallery/

images: 
  - image_path: /assets/images/gallery/20230424_111012.jpg
    title: Bison
    alt: bison in the sagebrush
    author: Ronan Hart 
    location: Yellowstone, WY
    date: 2023-04-24
    width: 100%
  - image_path: /assets/images/gallery/20230728_103140.jpg
    title: A small mushroom pushing through the leaf litter
    alt: A small orange mushroom pushing through the leaf litter with moss in the foreground
    author: Ronan Hart 
    location: Virginia
    date: 2023-07-28
    width: 100%
  - image_path: /assets/images/gallery/20240524_140506.jpg
    title: a prickly pear magenta flower
    alt: test2
    author: Ronan Hart 
    location: Albuquerque, NM
    date: 2024-05-24
    width: 50%
  - image_path: /assets/images/gallery/20240524_151807.jpg
    title: a yucca and its flowers
    alt: test2
    author: Ronan Hart 
    location: Albuquerque, NM
    date: 2024-05-24
    width: 50%
  - image_path: /assets/images/gallery/20240527_150300.jpg
    title: a prickly pear yellow flower
    alt: test2
    author: Ronan Hart 
    location: Albuquerque, NM
    date: 2024-05-27
    width: 50%
  - image_path: /assets/images/gallery/20240601_175113.jpg
    title: A magenta flower of a small barrel cactus
    alt: test2
    author: Ronan Hart 
    location: Arizona
    date:  2024-06-01
    width: 50%
  - image_path: /assets/images/gallery/20241103_114431.jpg
    title: Lichen growing on a branch
    alt: a branch with many different cup-like lichens of colors like orange-yellow, sage, and forest green. Some frost and snow is on the branch.
    author: Ronan Hart 
    location: Sandia Crest, Albuquerque, NM
    date:  2024-11-03
    width: 100%
  - image_path: /assets/images/gallery/20210324_153010.jpg
    title: Juniper
    alt: a juniper tree growing tall, growing in red-orange earth surrounded by some small shrubs earth. The sky in the background is bright blue
    author: Ronan Hart 
    location: Moab, UT
    date: 2021-03-24
    width: 50%
  
---

dev note: 
- want to figure out how to have each image it's own markdown file and pulled from there like [this](https://learn.cloudcannon.com/jekyll/photo-gallery/)
- want to have in a grid
- want to organize by year (ie each year is a section)

{% assign sorted_gallery = page.images | sort: 'date' %}
<ul class="photo-gallery">
  {% for image in sorted_gallery %}
    <figure>
      <a href="{{ image.image_path }}" class="image-popup" title="{{ image.title }}. Photo by {{ image.author }}. {{ image.location }}. {{ image.date }}">
        <img src="{{ image.image_path }}" alt="{{ image.alt }}" style="width:{{ image.width }}">
      </a>
    </figure>
  {% endfor %}
</ul>