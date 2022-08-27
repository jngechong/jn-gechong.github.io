---
layout: dark
title: About
example: "Example text."
---

This page describes the amazing {{ site.title }} by {{ site.author.name }}.
{{ page.example }}

{% include big-cat.html %}

## About Pages

The About Page is a common convention found on websites.

It is your opportunity to let us know all the details "about" your project:

- focus and topic area
- people involved
- code and projects ysed

{% for i in site.data.animals %}
- The {{ i.name }} is a {{ i.size }} animal.
{% endfor %}

## Large animal are special

{% for i in site.data.animals %}
{% if i.size == "large" %}- <strong style="color: {{ i.color }};">{{ i.name }}</strong>
{% else %}- <small>{{ i.name }}</small>
{% endif %}
{% endfor %}

## Small animal only

{% assign small_animals = site.animals | where: "size", "small" %}
{% for i in small_animals %}
- {{ i.name | upcase }}
{% endfor %}
