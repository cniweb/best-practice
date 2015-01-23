---
layout: default
title: Tags
---
<div id="post-content">
  <h2>Articles by Tags:</h2>
  <ul>
  {% for tag in site.tags %}
    <li><a name="{{ tag | first }}">{{ tag | first }}</a>
      <ul>
      {% for posts in tag %}
        {% for post in posts %}
          <li><a href="{{ post.url }}">{{ post.title }}</a></li>
        {% endfor %}
      {% endfor %}
      </ul>
    </li>
  {% endfor %}
  </ul>
</div>