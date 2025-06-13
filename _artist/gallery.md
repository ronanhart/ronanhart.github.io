---
title: Gallery
permalink: /gallery/
---

{% assign sorted_gallery = site.photo_gallery | sort: 'date' %}

{% include my-portfolio.html images=sorted_gallery %}