---
layout: page
title: Outline workflows
permalink: /workflows/
---

Workflows:

<ul>
    {% assign sorted = (site.workflows | sort: 'date') %}
    {% for item in sorted %}
<li><a href="{{ item.url }}">{{ item.title }}</a></li>
    {% endfor %}
</ul>

