---
layout: page
title: Trips
---

# Travel Planning

This section contains trip itineraries, packing lists, and travel notes.

## Destinations

{% assign trips = site.pages | where_exp: "item", "item.path contains 'trips/' and item.path != 'trips/index.md'" | sort: "date" | reverse %}

{% if trips.size > 0 %}
<ul class="post-list">
  {% for trip in trips %}
    <li>
      <h3>
        <a class="post-link" href="{{ trip.url | relative_url }}">
          {{ trip.title | default: trip.path | split: "/" | last | split: "." | first | replace: "-", " " | capitalize }}
        </a>
      </h3>
      {% if trip.date %}
        <span class="post-meta">{{ trip.date | date: site.minima.date_format }}</span>
      {% endif %}
      {% if trip.description %}
        <p>{{ trip.description }}</p>
      {% endif %}
    </li>
  {% endfor %}
</ul>
{% else %}
<p><em>No trip plans uploaded yet. Check back soon!</em></p>
{% endif %}

<p><em>To add your own trip plans, create markdown files in this directory.</em></p> 