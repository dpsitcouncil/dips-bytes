---
layout: default
title: Staff
permalink: /archive/
---

<h1>Archives</h1>

<h2>By year</h2>
<ul>
  {% assign years = "" | split: "" %}
  {% for post in site.posts %}
    {% capture post_year %}{{ post.date | date: "%Y" }}{% endcapture %}
    {% unless years contains post_year %}
      <li><a href="{{ post_year | prepend: '/' }}">{{ post_year }}</a></li>
      {% assign years = years | push: post_year %}
    {% endunless %}
  {% endfor %}
</ul>

<h2>By category</h2>
<ul>
  {% for category in site.categories %}
    <li><a href="{{ category[0] | prepend: '/category/' }}">{{ category[0] | capitalize }}</a></li>
  {% endfor %}
</ul>