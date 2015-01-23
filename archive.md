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
      <li>{{ post.date | date_to_string }}
        <ul>
          <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
        </ul>
      </li>
    {% endfor %}
  </ul>
</div>
