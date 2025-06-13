---
title: Gallery2
permalink: /gallery2/
---

{% assign sorted_gallery = site.gallery_photo | sort: 'date' %}

{% include my-gallery.html images=sorted_gallery %}