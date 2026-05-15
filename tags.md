---
layout: page
title: Themes and tags
permalink: /tags/
---

Here are all the themes (or tags) used on this site:

{% assign tag_pages = site.pages | where_exp: "item", "item.url contains '/tags/'" | sort: "title" %}
<ul>
{% for tag in tag_pages %}
{% unless tag.url == '/tags/' %}
<li><a href="{{ tag.url }}">{{ tag.title }}</a></li>
{% endunless %}

{% endfor %}
</ul>