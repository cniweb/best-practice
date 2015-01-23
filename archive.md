---
layout: default
title: Archive
---

<header id="post-header">
    <h1 id="post-title">{{ page.title }}</h1>
    <h4 id="post-subtitle">Blog Posts:</h4>
</header>

<div id="post-content">
  <ul>
    {% for post in site.posts %}
      {% capture post_year %}{{ post.date | date: '%Y' }}{% endcapture %}
      {% if forloop.first %}
        <li>{{ post_year }}
      {% endif %}
      {% if forloop.first == false %}
          <ul>
            <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
          </ul>
      {% endif %}
      {% if forloop.last %}
        </li>
      {% endif %}
    {% endfor %}
  </ul>
</div>
