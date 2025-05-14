---
title: "Our Farm"
permalink: /our-farm/
layout: single
author_profile: false
---

### A Visual Look at Life on the Farm

Take a tour of MB Coffee's home in **Guji, Ethiopia** — from hand-picking ripe cherries to sun-drying and community-powered processing.

Our farm is more than a place — it's a story of heritage, care, and quality in every bean.

---

{% include gallery id="guji-gallery" caption="true" %}

{% assign gallery_images = site.static_files | where_exp: "file", "file.path contains '/assets/images/' and file.name contains 'gallery'" | sort: "name" %}
<div class="gallery" id="guji-gallery">
  {% for image in gallery_images %}
    <figure style="margin: 1rem 0;">
      <img src="{{ image.path }}" alt="MB Coffee - farm photo" style="width:100%; border-radius: 8px;" />
      <figcaption style="text-align: center; font-size: 0.9rem; color: #666;">
        {% case image.name %}
          {% when 'gallery1.jpeg' %} Hand-sorting green coffee under shade for quality control
          {% when 'gallery2.jpeg' %} Our team and community gathered at the farm's hub
          {% when 'gallery3.jpeg' %} Careful drying ensures even moisture and quality
          {% when 'gallery4.jpeg' %} Guji’s fertile land — where it all begins
          {% when 'gallery5.jpeg' %} Ripe cherries, hand-picked at peak ripeness
          {% when 'gallery6.jpeg' %} Sun-drying cherries for flavor clarity and consistency
          {% when 'gallery7.jpeg' %} Raised beds enhance air flow for even drying
          {% when 'gallery8.jpeg' %} Daily inspections during drying for optimal results
        {% endcase %}
      </figcaption>
    </figure>
  {% endfor %}
</div>

