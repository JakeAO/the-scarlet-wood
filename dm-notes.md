---
layout: page
title: DM Notes
permalink: /dm-notes/
---

{% assign groups = site.dm | group_by: "topic" | sort: 'topic' %}
{% for group in groups %}
<h3>{{ group.name }}</h3>
<ul>
{% assign items = group.items | sort: 'title' %}
{% for doc in items %}
  <li><a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
{% endfor %}
</ul>
{% endfor %}