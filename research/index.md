---
layout: page
title: Research
---

# Research

This section contains research notes, findings, and reference materials.

## Topics

{% assign topics = site.pages | where_exp: "item", "item.path contains 'research/' and item.path != 'research/index.md'" | sort: "date" | reverse %}

{% if topics.size > 0 %}
<ul class="post-list">
  {% for topic in topics %}
    <li>
      <h3>
        <a class="post-link" href="{{ topic.url | relative_url }}">
          {{ topic.title | default: topic.path | split: "/" | last | split: "." | first | replace: "-", " " | capitalize }}
        </a>
      </h3>
      {% if topic.date %}
        <span class="post-meta">{{ topic.date | date: site.minima.date_format }}</span>
      {% endif %}
      {% if topic.description %}
        <p>{{ topic.description }}</p>
      {% endif %}
    </li>
  {% endfor %}
</ul>
{% else %}
<p><em>No research topics uploaded yet. Check back soon!</em></p>
{% endif %}

<p><em>To add your own research, create markdown files in this directory.</em></p>

## All Research Topics

- [Research Topic 1](research_topic_1.md)
- [Research Topic 2](research_topic_2.md) 