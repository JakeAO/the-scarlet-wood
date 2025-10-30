---
layout: page
title: Players
description: Player-facing articles and resources for The Scarlet Wood.
permalink: /players/
---

# Players

Below are all player-facing articles. Articles are grouped by topic and ordered by title.

{% assign items = site.player | sort: 'title' %}
<ul>
{% for doc in items %}
  <li><a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
{% endfor %}
</ul>
