---
layout: page
title: Sessions
description: Player-facing session summaries for The Scarlet Wood.
permalink: /sessions/
---

Below are all player-facing session summaries grouped by act and ordered by session number.

{% assign items = site.sessions | sort: 'index' %}
{% assign grouped = items | group_by: 'act' | sort: 'name' %}

{% for group in grouped %}
<h2>Act {{ group.name }}</h2>
<ul>
{% for doc in group.items %}
  <li><a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
{% endfor %}
</ul>
{% endfor %}
