---
layout: page
width: xsmall
title: Notes
permalink: /notes/
---

{% assign notes = site.data.notes | sort: "title" %}
{% for note in notes %}
- **{{ note.title }}** - {{ note.notes }}
{% endfor %}