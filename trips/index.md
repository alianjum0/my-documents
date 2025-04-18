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

## All Trips

- [Alps Road Trip](alps_road_trip.md)
- [Alps Road Trip V2](alps_road_trip_v2.md)
- [Alps Road Trip V3](alps_road_trip_v3.md)
- [Family Adventure Guide](family_adventure_guide.md)
- [My Road Trip Swiss](my_road_trip_swiss.md)
- [Paris 2024](paris-2024.md) 