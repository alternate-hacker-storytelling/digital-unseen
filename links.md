---
layout: page
width: xsmall
title: Links
permalink: /links/
---

{% assign links = site.data.links | sort: "name" %}
{% for link in links %}
- **[{{ link.name }}]({{ link.link }})** - {{ link.description }}
{% endfor %}