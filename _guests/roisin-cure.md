---
layout: guest
published: true
title: "Róisín Curé"
first_name: Róisín
last_name: Curé
image: /img/guest/roisin-cure.jpg
image_alt: "A woman with long hair. She's smiling and holding a small shaggy dog."
tagline: "Comics artist and urban sketcher"
discipline: "Comics and sketching"
short_bio: "Róisín Curé is a Comics artist, an urban sketcher, author, and teacher based in Galway, Ireland. She teaches sketching worldwide and has published several books. Her current project is Wild Atlantic Ink, a monthly hand-drawn comic."
long_bio: "Róisín Curé is an urban sketcher, author, and teacher based in Galway, Ireland. She came to urban sketching in 2012 and built a practice around capturing everyday and natural scenes in ink and watercolour. She teaches sketching worldwide through online classes and in-person workshops, and has published illustrated books including An Urban Sketcher's Galway and The Urban Sketching Handbook: Drawing Expressive People. Her current project is Wild Atlantic Ink, a monthly hand-drawn comic."

intro_copy: 
quote_1: "In urban sketching they say draw verbs not nouns. I would say I'm a verb, I'm not a noun. I'm a doing. I'm not a being."
quote_2: "I've got the Ligne Claire of Hergé, and I have the Passion for Nature of David Attenborough, and the clown car is because I cannot be serious."
quote_3: "After about an hour I would get this feeling of calm, like a flow. Once the flow state began, I no longer made a mistake. My drawing would just happen automatically."
tags:
- comics
- urban-sketching
- ptsd
- ireland
- watercolor
- nature


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
