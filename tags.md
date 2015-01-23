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
  {% for post_tag in site.tags %}
    {% for data_tag in site.data.tags %}
      {% if data_tag.slug == post_tag %}
          {% assign tag = data_tag %}
      {% endif %}
    {% endfor %}
    <li>Tag: <a name="{{ tag.name | first }}" href="{{ site.baseurl }}/{{ tag.slug | first }}">{{ tag.name | first }}</a>
      <ul>
      {% for posts in tag %}
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