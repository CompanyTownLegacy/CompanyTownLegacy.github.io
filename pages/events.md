---
title: Community Events
layout: page
permalink: /events/
---

# Community Events

<div class="row">
{% assign events = site.data.events %}
{% for e in events %}
<div class="col-md-4"><img src="{{ e.image | prepend: '/objects/' | relative_url }}" alt="{{ e.image_alt }}" class="img-fluid"></div>
<div class="col-md-8">
<h4>{{ e.title }}</h4>
<p>{{ e.date }}. {{ e.description }}</p>
</div>
{% endfor %}
</div>
