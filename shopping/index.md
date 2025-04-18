---
layout: page
title: Shopping
---

# Shopping Lists

This section contains shopping lists and product research.

## Lists

{% assign lists = site.pages | where_exp: "item", "item.path contains 'shopping/' and item.path != 'shopping/index.md'" | sort: "date" | reverse %}

{% if lists.size > 0 %}
<ul class="post-list">
  {% for list in lists %}
    <li>
      <h3>
        <a class="post-link" href="{{ list.url | relative_url }}">
          {{ list.title | default: list.path | split: "/" | last | split: "." | first | replace: "-", " " | capitalize }}
        </a>
      </h3>
      {% if list.date %}
        <span class="post-meta">{{ list.date | date: site.minima.date_format }}</span>
      {% endif %}
      {% if list.description %}
        <p>{{ list.description }}</p>
      {% endif %}
    </li>
  {% endfor %}
</ul>
{% else %}
<p><em>No shopping lists uploaded yet. Check back soon!</em></p>
{% endif %}

<p><em>To add your own lists, create markdown files in this directory.</em></p>

## All Shopping Lists

- [Groceries](groceries.md) 