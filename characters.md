---
layout: page
width: xsmall
title: Characters
permalink: /characters/
---

{% assign characters = site.data.characters | sort: "name" %}
{% for character in characters %}
- **{{ character.name }}** - {{ character.description }}
{% endfor %}