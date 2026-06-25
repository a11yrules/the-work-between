---
layout: podcast
title: "Róisín Curé on comics and urban sketching"
published: true
type: podcast
summary: "Róisín Curé talks about finally calling herself a comics creator after years of resisting labels, and about her new monthly comic Wild Atlantic Ink. The conversation moves through drawing from life versus photos, what years of sketching built in her hands, and the calm that sketching brings to a mind that has long carried melancholy. It ends up somewhere unexpected, with foraged food and homemade bread."

permalink: /episodes/roisin-cure-on-comics-and-sketching/
# Podcast Episode Metadata
episode_type: full
episode_number: 03

# Audio Information
audio_file: 03-roisin-cure-sketching.mp3
audio_type: "audio/mpeg"
file_size: 134254352 # file size in bytes (required for podcast aggregators)
transcript_vtt: /assets/transcripts/show-03.vtt
transcript: transcripts/show-03.html

# Duration
duration: "PT55M56S"
duration_formatted: "55:56"

# Series
series: "The Work Between"

# Episode Artwork
cover_art: /img/covers/show-03-roisin-cure-3000.jpg
local_cover_art: /img/covers/show-03-roisin-cure-800.jpg
episode_image_linkedin: /img/covers/show-03-roisin-cure-linkedin.jpg

topics: ["Comics", "Urban Sketching"]

guest: "Róisín Curé"

date: 2026-06-24

# Author/Host
author: "Nic Steenhout"

# Content Rating
explicit: false

show-notes: /show-notes/show-03.md
# Categories/Tags
tags:
- comics
- urban-sketching
- ptsd
- ireland
- watercolor
- nature
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

