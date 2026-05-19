---
layout: podcast
title: "Mia Seljubac on watercolor and game development"
published: false
type: podcast
summary: "Mia Seljubac is a games lawyer who is building I Am the Cat, a cozy narrative game with fully hand-painted watercolor animation. Her visual style draws from illustrated children's books, and she animates every frame by hand on a light box. She talks about living with ADHD and a spinal injury and why she identifies as a maker who is disabled."

permalink: /episodes/mia-seljubac-on-watercolor-and-game-development/
# Podcast Episode Metadata
episode_type: full
episode_number: 01

# Audio Information
audio_file: 01-mia-seljubac-watercolog-game-dev.mp3
audio_type: "audio/mpeg"
file_size: 133289882 # file size in bytes (required for podcast aggregators)
transcript_vtt: /assets/transcripts/show-01.vtt
transcript: transcripts/show-01.html

# Duration
duration: "PT55M32S"
duration_formatted: "55:32"

# Series
series: "The Work Between"

# Episode Artwork
cover_art: /img/covers/show-01-mia-seljubac-3000.jpg
local_cover_art: /img/covers/show-01-mia-seljubac-800.jpg
episode_image_linkedin: /img/covers/show-01-mia-seljubac-linkedin-cover.jpg

topics: ["Watercolor", "Animation", "Game development"]

guest: "Mia Seljubac"

date: 2026-05-18

# Author/Host
author: "Nic Steenhout"

# Content Rating
explicit: false

show-notes: /show-notes/show-01.md
# Categories/Tags
tags:
- watercolor
- games
- adhd
- animation
- spinal-injury
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

