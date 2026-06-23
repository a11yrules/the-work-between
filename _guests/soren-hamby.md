---
layout: guest
published: false
title: "Soren Hamby"
first_name: Soren
last_name: Hamby
image: /img/guest/alessondra-springmann.jpg
image_alt: ""
tagline: ""
discipline: ""
short_bio: ""
long_bio: "Soren Hamby is an artist and advocate who survives under capitalism as an accessibility and product equity designer. Their natural state is to build systems, frameworks, and communities, and to challenge the hidden structures that determine inclusion. They live in New York’s lower Hudson Valley on unceded Ramapough Lenape land, reshaping perceptions of living with multiple disabilities and intersecting identities. When they’re not busy with small goals like changing the world, you’ll find them painting, doing fiber arts, writing poetry, or collecting different ways of making and creating, which they see as essential human needs.
"
intro_copy: 
quote_1: ""
quote_2: ""
quote_3: "."
tags:
- 


---

## About {{ page.first_name }}

<div class="guest-about-section">
{% if page.image %}
<span class="guest-list">
<img src="{{ page.image | relative_url }}" alt="{{ page.image_alt }}" class="guest-img">
</span>
{% endif %}

{% if page.long_bio %}
<div class="guest-bio-text">{{ page.long_bio }}</div>
{% endif %}
</div>


{% if page.quote_1 or page.quote_2 or page.quote_3 %}
## Quotes
{: .centered-heading }

  {% if page.quote_1 %}
> {{ page.quote_1 }}
  {% endif %}

  {% if page.quote_2 %}
> {{ page.quote_2 }}
  {% endif %}

  {% if page.quote_3 %}
> {{ page.quote_3 }}
  {% endif %}

{% endif %}

{% if page.tags %}
## Key themes

<ul>
{% for tag in page.tags %}
    {% assign tag_data = site.data.tags | where: "slug", tag | first %}
    <li><a href="/tags/{{ tag }}/">{{ tag_data.label }}</a></li>
  {% endfor %}
</ul>

{% endif %}

{% if page.links %}
## Links

<ul>
  {% for link in page.links %}
    <li><a href="{{ link.url }}">{{ link.label }}</a></li>
  {% endfor %}
</ul>

{% endif %}

{% assign episodes = site.posts | where: "guest", page.title %}
{% if episodes.size > 0 %}
## Featured conversation

  {% for post in episodes %}
  <img src="{{ post.local_cover_art}}" alt="" class="featured-conversation-image" />

{{ post.summary }}

  <a href="{{ post.url | relative_url }}">{{ post.title }}</a> &mdash; {{ post.date | date: "%B %d, %Y" }} &mdash; {{ post.duration_formatted }} 
  {% endfor %}

{% else %}
<p>No episodes found for this guest.</p>
{% endif %}
