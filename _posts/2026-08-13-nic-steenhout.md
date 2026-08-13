---
layout: podcast
title: "Nic Steenhout on quilting, sketching, and photography"
published: false
type: podcast
summary: "Mark Miller turns the tables and interviews Nic about his own creative practice. They talk about sketching, quilting and bird photography, why making things helps quiet Nic’s mind, and why the process matters more to him than the finished work. The conversation also touches on martial arts, self-criticism, vulnerability, and wanting to be seen as more than the disabled accessibility guy."

permalink: /episodes/nic-steenhout-on-quilting-sketching-and-photography/
# Podcast Episode Metadata
episode_type: full
episode_number: 05

# Audio Information
audio_file: 05-nic-steenhout-sketching.mp3
audio_type: "audio/mpeg"
file_size: 130917728 # file size in bytes (required for podcast aggregators)
transcript_vtt: /assets/transcripts/show-05.vtt
transcript: transcripts/show-05.html

# Duration
duration: "PT54M33S"
duration_formatted: "54:33"

# Series
series: "The Work Between"

# Episode Artwork
cover_art: /img/covers/show-05-nic-steenhout-3000.jpg
local_cover_art: /img/covers/show-05-nic-steenhout-800.jpg
episode_image_linkedin: /img/covers/show-05-nic-steenhout-linkedin.jpg

topics: ["Quilting", "Sketching", "Photography"]

guest: "Nic Steenhout"

date: 2026-08-13

# Author/Host
author: "Nic Steenhout"

# Content Rating
explicit: false

show-notes: /show-notes/show-05.md
# Categories/Tags
tags:
- photography
- quilting
- sketching
- digital-accessibility
- watercolor
- adhd
- mobility
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

