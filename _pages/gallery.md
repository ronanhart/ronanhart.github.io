---
title: ""
permalink: /artist/photos/
---

Click on each image to expand to full size and see more information on where and when the photo was taken.

---

{% assign sorted_gallery = site.gallery_photo | sort: 'date' %}

{% include my-portfolio.html images=sorted_gallery %}