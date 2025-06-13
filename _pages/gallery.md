---
title: Gallery
permalink: /gallery/
---

{% assign sorted_gallery = site.gallery_photo | sort: 'date' %}

{% include my-portfolio.html images=sorted_gallery %}