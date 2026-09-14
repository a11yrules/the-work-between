---
layout: podcast
title: "Nic Steenhout on learning urban sketching"
published: true
type: podcast
summary: "Nic Steenhout uses this solo episode to push back on standard urban sketching advice: draw from life, use ink, skip photos. He argues that advice assumes a non-disabled body and a brain that can tune out a busy street. Speaking from his own experience as a disabled sketcher, he separates scaffolding (photos, pencils, things you use while learning and can drop later) from accommodation (wheelchair access, noise control, things that don't go away once you've improved)."

permalink: /episodes/nic-steenhout-on-learning-urban-sketching/
# Podcast Episode Metadata
episode_type: full
episode_number: 06

# Audio Information
audio_file: 06-nic-on-urban-sketching.mp3
audio_type: "audio/mpeg"
file_size: 36118352 # file size in bytes (required for podcast aggregators)
transcript_vtt: /assets/transcripts/show-06.vtt
transcript: transcripts/show-06.html

# Duration
duration: "PT15M03S"
duration_formatted: "15:03"

# Series
series: "The Work Between"

# Episode Artwork
cover_art: /img/covers/show-06-nic-steenhout-3000.jpg
local_cover_art: /img/covers/show-06-nic-steenhout-800.jpg
episode_image_linkedin: /img/covers/show-06-nic-steenhout-linkedin.jpg

topics: ["Disability", "Urban Sketching", "Learning Styles"]

guest: "Nic Steenhout"

date: 2026-09-14

# Author/Host
author: "Nic Steenhout"

# Content Rating
explicit: false

show-notes: /show-notes/show-06.md
# Categories/Tags
tags:
- disability
- urban-sketching
- learning-styles
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

