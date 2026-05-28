---
layout: podcast
title: "Dr. Alessondra Springmann on quilting"
published: true
type: podcast
summary: "Planetary scientist Sondy Springmann turns worn-out clothes into quilts, combining secondhand materials, ninety-year-old sewing machines, and modern technology in unexpected ways. Along the way, we explore disability, creativity, community, and the problem-solving mindset that comes from living in a world that wasn’t designed for you."

permalink: /episodes/dr-alessondra-springmann-on-quilting/
# Podcast Episode Metadata
episode_type: full
episode_number: 02

# Audio Information
audio_file: 02-sondy-springmann-quilting.mp3
audio_type: "audio/mpeg"
file_size: 152612048 # file size in bytes (required for podcast aggregators)
transcript_vtt: /assets/transcripts/show-02.vtt
transcript: transcripts/show-02.html

# Duration
duration: "PT1H03M35S"
duration_formatted: "1:03:35"

# Series
series: "The Work Between"

# Episode Artwork
cover_art: /img/covers/show-02-sondy-springmann-3000.jpg
local_cover_art: /img/covers/show-02-sondy-springmann-800.jpg
episode_image_linkedin: /img/covers/show-02-sondy-springmann-linkedin.jpg

topics: ["Quilting"]

guest: "Dr. Alessondra Springmann"

date: 2026-05-28

# Author/Host
author: "Nic Steenhout"

# Content Rating
explicit: false

show-notes: /show-notes/show-02.md
# Categories/Tags
tags:
- quilting
- inflammatory-bowel-disease
- repetitive-strain-injury
- chronic-headaches
- laryngopharyngeal-reflux
---

<details>
    <summary><h2>Timed Transcript</h2></summary>
    <div id="timed-transcript-content"></div>
</details>

<details>
    <summary><h2>Static Transcript</h2></summary>
    
{% if page.transcript %}
  {% include {{ page.transcript }} %}
{% endif %}
</details>

{% if page.tags %}
## Key themes

<ul>
{% for tag in page.tags %}
    {% assign tag_data = site.data.tags | where: "slug", tag | first %}
    <li><a href="/tags/{{ tag }}/">{{ tag_data.label }}</a></li>
  {% endfor %}
</ul>

{% endif %}

{% if page.show-notes %}
## Show notes
  {% include {{ page.show-notes }} %}
{% endif %}

