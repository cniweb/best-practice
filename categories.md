---
layout: default
title: Categories
---
<div id="post-content">
  <h2>Articles by Category:</h2>
  <ul>
  {% for category in site.categories %}
    <li>Category:<a name="{{ category | first }}">{{ category | first }}</a>
      <ul>
      {% for posts in category %}
        {% for post in posts %}
          <li><a href="{{ post.url }}">{{ post.title }}</a></li>
        {% endfor %}
      {% endfor %}
      </ul>
    </li>
  {% endfor %}
  </ul>
</div>