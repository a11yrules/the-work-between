---
layout: guest
title: "Mia Seljubac"
first_name: Mia
last_name: Seljubac
image: /img/guest/mia-seljubac.jpg
image_alt: "A young woman with long dark brown hair and a smile."
tagline: "Watercolor illustrator, game developer, games lawyer"
discipline: "Watercolor, Game dev"
short_bio: "Mia Seljubac is a games lawyer turned game developer and co-founder of Cereal Mug Games. She's currently building I Am the Cat, a narrative game with fully watercolor animation. She also works in ink and acrylics."
long_bio: "Mia is a games lawyer turned game developer and co-founder of Cereal Mug Games. She's currently working on a cosy narrative game called 'I am the cat', where all the animation and textures are completely hand-painted in watercolour. Mia works in a variety of mediums, including ink, watercolour and acrylics, and sells hand-painted jackets at her local tattoo studio. "
intro_copy: 
quote_1: "I found out that 'video game lawyer' is a job that exists, so I kind of do law within the games industry for the love of it."
quote_2: "I let the watercolor do what it wants, and I like the feeling of it moving in weird ways that animation doesn't tend to"
quote_3: "I'd say that I'm a maker who is disabled. I prefer that. That feels more fitting to me."
tags:
- watercolor
- games
- adhd
- animation
- spinal-injury

links:
  - label: "Mia's game I am the cat"
    url: "https://store.steampowered.com/app/3719920/I_am_the_cat/"
  - label: "LinkedIn"
    url: "https://uk.linkedin.com/in/mia-seljubac-aab797122"


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

{% assign episodes = site.posts | where: "guest", "Nic Steenhout" %}
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
