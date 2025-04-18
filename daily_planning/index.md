---
layout: page
title: Daily Planning
---

# Daily Planning

This section contains daily planning documents, schedules, and task lists.

## Latest Plans

{% assign daily_planning_pages = site.pages | where_exp: "item", "item.path contains 'daily_planning/'" %}
{% assign filtered_pages = daily_planning_pages | reject: "path", "daily_planning/index.md" %}
{% assign plans = filtered_pages | sort: "date" | reverse %}

{% if plans.size > 0 %}
<ul class="post-list">
  {% for plan in plans %}
    <li>
      <h3>
        <a class="post-link" href="{{ plan.url | relative_url }}">
          {{ plan.title | default: plan.path | split: "/" | last | split: "." | first | replace: "-", " " | capitalize }}
        </a>
      </h3>
      {% if plan.date %}
        <span class="post-meta">{{ plan.date | date: site.minima.date_format }}</span>
      {% endif %}
      {% if plan.description %}
        <p>{{ plan.description }}</p>
      {% endif %}
    </li>
  {% endfor %}
</ul>
{% else %}
<p><em>No plans uploaded yet. Check back soon!</em></p>
{% endif %}

<p><em>To add your own plans, create markdown files in this directory.</em></p>

## All Daily Plans

- [Plan 1](plan_1.md)
- [Plan 2](plan_2.md) 