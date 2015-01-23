---
layout: default
title: Categories
---

<header id="post-header">
    <h1 id="post-title">{{ page.title }}</h1>
    <h4 id="post-subtitle">Articles by categories:</h4>
</header>

<div id="post-content">
  <ul>
  {% for post_category in site.categories %}
    {% for data_category in site.data.categories %}
      {% if data_category.slug == post_category %}
          {% assign category = data_category %}
      {% endif %}
    {% endfor %}
    <li>Category: <a href="{{ site.baseurl }}/{{ data_category.slug }}">{{ data_category.name }}</a>
      <ul>
      {% for posts in post_category %}
        {% if forloop.first == false %}
          {% for post in posts %}
            <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
          {% endfor %}
        {% endif %}
      {% endfor %}
      </ul>
    </li>
  {% endfor %}
  </ul>
</div>