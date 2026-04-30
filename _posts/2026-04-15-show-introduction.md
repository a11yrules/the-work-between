---
layout: podcast
title: "Introduction to The Work Between"
type: podcast
summary: "The Work Between is an interview podcast with disabled artists and creators. We will be discussing their creative processes and explore the intersection of creativity and disability, and asking how that intersection shapes identity."

permalink: /episodes/the-work-between-introduction/
# Podcast Episode Metadata
episode_type: full
episode_number: 00

# Audio Information
audio_url: 
audio_type: "audio/mpeg"
transcript_vtt: /assets/transcripts/the-work-between-introduction.vtt
transcript: transcripts/show-00.html

# Duration
duration: "PT6M06S"
duration_formatted: "6:06"

# Series
series: "The Work Between"

# Episode Artwork
cover_art: /img/covers/introduction-episode-cover-3000.jpg
local_cover_art: /img/covers/introduction-episode-cover-800.jpg

topics: ["", ""]

guest: "Nic Steenhout"

date: 2026-04-15

# Author/Host
author: "Nic Steenhout"

# Content Rating
explicit: false

show-notes: /show-notes/show-00.html
# Categories/Tags

tags: 
---


<div class="audio-container">

<h2>Listen to the episode</h2>
<audio id="audio1" data-able-player preload="auto" data-heading-level="2" data-speed-icons="animals" data-root-path="/podcast-dev/assets/ableplayer/" data-transcript-div="timed-transcript-content">
  <source type="audio/mpeg" src="{{ page.audio_url }}"/>
  <track kind="captions" src="{{ page.transcript_vtt }}" srclang="en" label="English transcript"/>
</audio>

</div>
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


{% if page.show-notes %}
  {% include {{ page.show-notes }} %}
{% endif %}


