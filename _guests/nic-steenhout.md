---
layout: guest
title: "Nic Steenhout"
first_name: Nic
last_name: Steenhout
image: /img/guest/nic-steenhout.jpg
image_alt: "A middle aged white man with short brown hair. He wears glasses with a thing oval black rim."
tagline: "Quilter, bird photographer, digital accessibility consultant"
discipline: "Quilting, photography, sketching"
short_bio: "Nic Steenhout is the host and creator of The Work Between. A quilter, bird photographer, and sketcher, he also brings 25+ years of digital accessibility expertise to his work as a speaker, trainer, and consultant. He lives in British Columbia."
long_bio: "Nic Steenhout is the host and creator of The Work Between. A quilter, bird photographer, and sketcher, he brings his own creative practice to every conversation on the show. He has spent more than 25 years working in digital accessibility as a speaker, trainer, and consultant. He has worked with disabled people, non-profits, government organizations, and corporations across three continents. He also hosts A11y Rules, a podcast dedicated to web accessibility. Nic lives and works in British Columbia."
intro_copy: 
quote_1: 
quote_2:
quote_3:
tags:
- "Quilting"
- "Photography"
- "Sketching"
- "Digital accessibility"

links:
  - label: "Business website"
    url: "https:nicolas-steenhout.com"
    - label: "Nic's Art Journey"
    url: "https://artjourney.nicolas-steenhout.com"
  - label: "LinkedIn"
    url: "https://www.linkedin.com/in/nicolassteenhoute"


---

## About {{ page.first_name }}

{% if page.image %}
      <span class="guest-list">
      <img src="{{ page.image | relative_url }}" alt="" class="guest-img">
      </span>
      {% endif %}

{% if page.long_bio %}
  {{ page.long_bio }}
{% endif %}


{% if page.quote_1 or page.quote_2 or page.quote_3 %}
## Quotes

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
    <li>{{ tag }}</li>
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
  <img src="{{ post.local_cover_art}}" alt="" />

{{ post.summary }}

  <a href="{{ post.url | relative_url }}">{{ post.title }}</a> &mdash; {{ post.date | date: "%B %d, %Y" }} &mdash; {{ post.duration_formatted }} 
  {% endfor %}

{% else %}
<p>No episodes found for this guest.</p>
{% endif %}
