---
layout: page
title: Episode list
permalink: /episodes/
---

<ul>
{% for post in site.posts %}
  <li class="episode-list-item">
    {% if post.cover_art %}
      <img src="{{ post.local_cover_art | relative_url }}" alt="" loading="lazy" class="episode-list-cover">
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