---
layout: podcast
title: "Soren Hamby on poetry and fiber arts"
published: true
type: podcast
summary: "Soren Hamby, poet and disability rights advocate, talks poetry as necessity and expression, the craft of specificity and editing, and living with vision loss and late-diagnosed neurodivergence. A candid look at writing as self-reflection, advocacy, and a way to make disability's realities understood."

permalink: /episodes/soren-hamby-on-poetry/
# Podcast Episode Metadata
episode_type: full
episode_number: 04

# Audio Information
audio_file: 04-soren-hamby-poetry.mp3
audio_type: "audio/mpeg"
file_size: 134445404 # file size in bytes (required for podcast aggregators)
transcript_vtt: /assets/transcripts/show-04.vtt
transcript: transcripts/show-04.html

# Duration
duration: "PT55M01S"
duration_formatted: "56:01"

# Series
series: "The Work Between"

# Episode Artwork
cover_art: /img/covers/show-3-soren-hamby-3000.jpg
local_cover_art: /img/covers/show-3-soren-hamby-800.jpg
episode_image_linkedin: /img/covers/show-3-soren-hamby-linkedin.jpg

topics: ["Poetry and fiber arts"]

guest: "Soren Hamby"

date: 2026-07-22

# Author/Host
author: "Nic Steenhout"

# Content Rating
explicit: false

show-notes: /show-notes/show-04.md
# Categories/Tags
tags:
- poetry
- vision-loss
- neurodivergence
- fiber-arts
- lgbtq+
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

