---
layout: page
title: Rules & Info
description: Player-facing info, resources, and rules-clarifications.
permalink: /info/
---

Below are all player-facing articles. Articles are grouped by topic and ordered by title.

{% assign groups = site.info | group_by: "topic" | sort: 'title' %}
{% for group in groups %}
<h3>{{ group.name }}</h3>
<ul>
{% assign items = group.items | sort: 'title' %}
{% for doc in items %}
  <li><a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
{% endfor %}
</ul>
{% endfor %}