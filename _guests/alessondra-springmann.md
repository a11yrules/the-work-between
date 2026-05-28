---
layout: guest
title: "Dr. Alessondra Springmann"
first_name: Alessondra
last_name: Springmann
image: /img/guest/alessondra-springmann.jpg
image_alt: "A young woman with long dark brown hair and a smile."
tagline: "Planetary scientist and quilter"
discipline: "Quilting"
short_bio: "Dr. Alessondra “Sondy” Springmann is a planetary scientist and quilter who turns secondhand fabrics and worn work clothes into quilts that preserve stories, memories, and history."
long_bio: "Dr. Alessondra “Sondy” Springmann is a planetary scientist and quilter based in Colorado. She earned her PhD from the Lunar and Planetary Laboratory at the University of Arizona and has spent her career studying asteroids, comets, and other small bodies across the solar system. Her work has included the NASA OSIRIS-REx asteroid sample return mission and planetary radar observations at the Arecibo Observatory in Puerto Rico. Away from science, Sondy creates quilts from secondhand fabrics, worn work clothes, and reclaimed materials. Her work combines traditional sewing techniques with modern tools such as laser cutters, transforming everyday textiles into objects that carry stories, memories, and history. Through both science and quilting, she is drawn to understanding how things are built, how they change over time, and how creative problem-solving helps us make sense of the world."
intro_copy: 
quote_1: "I think those of us who’ve been forced to look at the world differently, I think we get to make more interesting choices about what we make."
quote_2: "Disabled people have thought about how they move through the world, how they interact with the world, and whether it’s their choice or otherwise, they have had to think deeply about the fundamental tenets that society expects"
quote_3: "It's just fabric, Nic. No one's going to get food poisoning."
tags:
- quilting
- inflammatory-bowel-disease
- repetitive-strain-injury
- chronic-headaches
- laryngopharyngeal-reflux


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
