---
layout: page
width: xsmall
title: Categories
permalink: /categories/
---

{% assign all_categories = '' %}

{% assign links = site.data.links %}
{% for link in links %}
    
    {% for category in link.categories %}

        {% assign already = 0 %}

        {% if all_categories contains category %}
            {% assign already = 1 %}
        {% endif %}
    
        {% if already == 0 and category != '' %}
            {% assign all_categories = all_categories | append: ',' | append: category %}
        {% endif %}

    {% endfor %}

{% endfor %}

{% assign notes = site.data.notes %}
{% for note in notes %}
    
    {% for category in note.categories %}

        {% assign already = 0 %}

        {% if all_categories contains category %}
            {% assign already = 1 %}
        {% endif %}
    
        {% if already == 0 and category != '' %}
            {% assign all_categories = all_categories | append: ',' | append: category %}
        {% endif %}

    {% endfor %}

{% endfor %}

{% assign posts = site.posts %}
{% for post in posts %}
    
    {% for category in post.categories %}

        {% assign already = 0 %}

        {% if all_categories contains category %}
            {% assign already = 1 %}
        {% endif %}
    
        {% if already == 0 and category != '' %}
            {% assign all_categories = all_categories | append: ',' | append: category %}
        {% endif %}

    {% endfor %}

{% endfor %}


{% assign categories = all_categories | split: "," | sort %}

<ul>
{% for category in categories %}
    {% if category != '' %}
        <li><strong>{{ category }}</strong></li>
    {% endif %}
{% endfor %}
</ul>