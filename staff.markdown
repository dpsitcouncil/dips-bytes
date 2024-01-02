---
layout: default
title: Staff
permalink: /staff/
---

<h1>Staff</h1>

<div class="author-list">
  {% for author in site.authors %}
    <div class="item">
      <a class="author-link" href="{{ site.baseurl }}{{ author.url }}">
        <!-- <div class="post-meta">{{ post.date | date: date_format }}</div> -->
        <div class="author-image">
          {% if author.image %} <img src="{{author.image}}">
          {% endif %}
        </div>
        <div class="author-name-section">
          <div class="author-name">{{ author.display_name  }}</div>
          <div class="author-position">{{ author.position }}</div>
        </div>
      </a>
    </div>
  {%- endfor -%}
</div>
