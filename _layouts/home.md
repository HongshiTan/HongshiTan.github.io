---
layout: about
title: ""
author: "TAN Hongshi (谭洪仕)"
---

{% include main.md sticky='true' %}

<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.15.4/css/all.css">
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.15.4/css/v4-shims.css">
<h2 class="tags-item-label">INTERESTS</h2>
<br>
<br>

<i class="fa fa-camera-retro" aria-hidden="true" style="font-size:36px"></i>
&thinsp; &thinsp; &thinsp;
<i class="fas fa-guitar" aria-hidden="true" style="font-size:36px"></i>
&thinsp; &thinsp; &thinsp;
<i class="fa fa-bicycle" aria-hidden="true" style="font-size:36px"></i>
&thinsp; &thinsp; &thinsp;
<i class="fas fa-cat" aria-hidden="true" style="font-size:36px"></i>
&thinsp; &thinsp; &thinsp;
<i class="fas fa-atom" aria-hidden="true" style="font-size:36px"></i>


<br>

<h2 class="tags-item-label">POSTS</h2>

<br>

<div class="catalogue">
  {% for post in site.posts %}
    {% if post.sticky %}
      {% include catalogue_item.html sticky='true' %}
    {% endif %}
  {% endfor %}

  {% for post in paginator.posts %}
    {% include catalogue_item.html %}
  {% endfor %}
</div>

<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path | prepend: site.baseurl }}" class="left arrow">&#8592;</a>
  {% endif %}
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path | prepend: site.baseurl }}" class="right arrow">&#8594;</a>
  {% endif %}

  <span>{{ paginator.page }}</span>
</div>


