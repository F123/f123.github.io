---
layout: page
title: Outline workflows
permalink: /workflows/
---


In this collection I will add workflow outlines to detail such things
as:

<ul>
    {% assign sorted = (site.workflows | sort: 'date') %}
    {% for item in sorted %}
<li><a href="{{ item.url }}">{{ item.title }}</a></li>
    {% endfor %}
</ul>

