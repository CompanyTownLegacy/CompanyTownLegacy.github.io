---
title: Contributors
layout: page
permalink: /contributors/
---

# Contributors

A wide group of folks have contributed the the Company Town Legacy project, from university students to community historians. 
This page recognizes some of our contributors.

{% assign people = site.data.contributors %}
{% for p in people %}
- {{ p.name }} {% endfor %}
