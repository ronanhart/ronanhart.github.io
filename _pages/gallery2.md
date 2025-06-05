---
title: Gallery2
permalink: /gallery2/
---

{% assign sorted_gallery = site.photo_gallery | sort: 'date' %}

{% include my-portfolio.html images=sorted_gallery %}