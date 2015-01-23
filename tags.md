---
layout: default
title: Tags
---

<header id="post-header">
    <h1 id="post-title">{{ page.title }}</h1>
    <h4 id="post-subtitle">Articles by tags:</h4>
</header>

<div id="post-content">
  <ul>
  {% for tag in site.tags %}
    <li>Tag: <a name="{{ tag | first }}">{{ tag | first }}</a>
      <ul>
      {% for posts in tag %}
        {% for post in posts %}
          <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
        {% endfor %}
      {% endfor %}
      </ul>
    </li>
  {% endfor %}
  </ul>
</div>