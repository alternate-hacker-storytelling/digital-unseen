---
layout: page
width: xsmall
title: Vocabulary
permalink: /vocabulary/
---

{% assign vocabulary = site.data.vocabulary | sort: "name" %}
{% for voc in vocabulary %}
- **{{ voc.name }}** - {{ voc.description }}
{% endfor %}