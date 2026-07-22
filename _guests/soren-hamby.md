---
layout: guest
published: true
title: "Soren Hamby"
first_name: Soren
last_name: Hamby
image: /img/guest/soren-hamby.jpg
image_alt: "Soren, a nonbinary person with short gray hair and pale skin, wearing glasses and a black shirt, smiling brightly with an upturned face, radiating sparkling optimism"
tagline: "Poet and fiber artist"
discipline: "Poetry, Crochetting, Knitting"
short_bio: "Soren Hamby is an artist, advocate, and accessibility and product equity designer who challenges hidden structures around inclusion while living with multiple disabilities. Outside of work, they paint, write poetry, and do fiber arts."
long_bio: "Soren Hamby is an artist and advocate who survives under capitalism as an accessibility and product equity designer. Their natural state is to build systems, frameworks, and communities, and to challenge the hidden structures that determine inclusion. They live in New York’s lower Hudson Valley on unceded Ramapough Lenape land, reshaping perceptions of living with multiple disabilities and intersecting identities. When they’re not busy with small goals like changing the world, you’ll find them painting, doing fiber arts, writing poetry, or collecting different ways of making and creating, which they see as essential human needs."
intro_copy: 
quote_1: "I think doubting is part of the process. I think if you're ever sure of anything, then you're probably wrong."
quote_2: "Disability... is a completely neutral thing, like water. It is just there. It can be good and can shape my life in ways that I never thought it would. It can also—too much of it can be a lot to carry."
quote_3: "When I'm editing a poem, I don't just write it down and then it's done. I write it. I sit there. I edit it. I probably edit it again. I edit it with one person. Then I take it to a writing group... so it probably goes through three to four rounds before it ever would see a stranger's eyes or ears."
tags:
- poetry
- vision-loss
- neurodivergence
- fiber-arts
- lgbtq+


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
