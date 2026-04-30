---
layout: default
title: Episode list
permalink: /episodes/
---

<h1>Episode list</h1>

<ul>
{% for post in site.posts %}
  <li>
    {% if post.cover_art %}
      <img src="{{ post.local_cover_art | relative_url }}" alt="Cover art for {{ post.title }}">
    {% endif %}
    <div>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      {% if post.guest %}
        <p>Guest: {{ post.guest }} |
      {% endif %}
      {% if post.topics %}
        Topics: {{ post.topics | join: ", " }} |
      {% endif %}
      Published: {{ post.date | date: "%B %d, %Y" }}</p>
    </div>
  </li>
{% endfor %}
</ul>