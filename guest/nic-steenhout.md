---
layout: guest
title: "Nic Steenhout"
permalink: /guest/nic-steenhout/
---

{% assign episodes = site.posts | where: "guest", "Nic Steenhout" %}
{% if episodes.size > 0 %}
<ul>
  {% for post in episodes %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> &mdash; {{ post.date | date: "%B %d, %Y" }}</li>
  {% endfor %}
</ul>
{% else %}
<p>No episodes found for this guest.</p>
{% endif %}
