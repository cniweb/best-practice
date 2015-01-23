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
  {% for category in site.categories %}
    <li>Category: <a name="{{ category | first }}">{{ category | first }}</a>
      <ul>
      {% for posts in category %}
        {% for post in posts %}
          {% if forloop.first == false %}
            <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
          {% endif %}
        {% endfor %}
      {% endfor %}
      </ul>
    </li>
  {% endfor %}
  </ul>
</div>