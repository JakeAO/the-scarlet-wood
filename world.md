---
layout: page
title: World
description: Player-facing articles and resources for The Scarlet Wood.
permalink: /world/
---

Below are all player-facing articles. Articles are grouped by topic and ordered by title.

{% assign groups = site.world | group_by: "topic" | sort: 'title' %}
{% for group in groups %}
<h3>{{ group.name }}</h3>
<ul>
{% assign items = group.items | sort: 'title' %}
{% for doc in items %}
  <li><a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
{% endfor %}
</ul>
{% endfor %}
