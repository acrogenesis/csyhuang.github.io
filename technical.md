---
layout: page
title: Technical Notes
permalink: /technical/
---

It's fun to write about what I have learnt and share solutions to technical problems I have solved.

## Data Science

{% for post in site.tags.ds %}
 - [{{ post.title }}]({{ post.url }})
{% endfor %}

## Software Engineering

{% for post in site.tags.se %}
 - [{{ post.title }}]({{ post.url }})
{% endfor %}

## System / Package set-up

{% for post in site.tags.setup %}
 - [{{ post.title }}]({{ post.url }})
{% endfor %}

## Notes taken from lectures / online courses:

{% for post in site.tags.coursenotes %}
 - [{{ post.title }}]({{ post.url }})
{% endfor %}

