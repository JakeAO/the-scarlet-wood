---
layout: page
title: Sessions
description: Player-facing session summaries for The Scarlet Wood.
permalink: /sessions/
---

Below are all player-facing articles. Articles are ordered by session number.

{% assign items = site.sessions | sort: 'index' %}
<ul>
{% for doc in items %}
  <li><a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
{% endfor %}
</ul>
