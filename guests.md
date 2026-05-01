---
layout: page
title: Guests
permalink: /guests/
---

{% comment %} Build alphabetical navigation {% endcomment %}
<nav aria-label="Jump to letter">
  <ul>
  {% assign letters = "a,b,c,d,e,f,g,h,i,j,k,l,m,n,o,p,q,r,s,t,u,v,w,x,y,z" | split: "," %}
  {% for letter in letters %}
    {% assign has_guests = false %}
    {% for guest in site.data.guests %}
      {% assign first_letter = guest.last_name | slice: 0 | downcase %}
      {% if first_letter == letter %}
        {% assign has_guests = true %}
        {% break %}
      {% endif %}
    {% endfor %}
    {% if has_guests %}
    <li><a href="#{{ letter }}">{{ letter }}</a></li>
    {% endif %}
  {% endfor %}
  </ul>
</nav>

{% comment %} Group and display guests by last name initial {% endcomment %}
{% assign sorted_guests = site.data.guests | sort: "last_name" %}
{% assign letters = "a,b,c,d,e,f,g,h,i,j,k,l,m,n,o,p,q,r,s,t,u,v,w,x,y,z" | split: "," %}

{% for letter in letters %}
  {% assign letter_guests = "" | split: "" %}
  {% for guest in sorted_guests %}
    {% assign first_letter = guest.last_name | slice: 0 | downcase %}
    {% if first_letter == letter %}
      {% assign letter_guests = letter_guests | push: guest %}
    {% endif %}
  {% endfor %}
  
  {% if letter_guests.size > 0 %}
  <section>
    <h2 id="{{ letter }}">{{ letter | upcase }}</h2>
    
    {% for guest in letter_guests %}
    <article>
      <h3>{{ guest.last_name }}, {{ guest.first_name }}</h3>
      {% if guest.image %}
      <span class="guest-list">
      <img src="{{ guest.image | relative_url }}" alt="" class="guest-img">
      </span>
      {% endif %}
      <p>{{ guest.bio }}</p>
      {% if guest.url %}
      <p><a href="{{ guest.url }}">View all episodes with {{ guest.first_name }} {{ guest.last_name }}</a></p>
      {% endif %}
    </article>
    {% endfor %}
  </section>
  {% endif %}
{% endfor %}