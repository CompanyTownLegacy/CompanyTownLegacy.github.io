---
title: Community Events
layout: page
permalink: /events/
---

# Community Events

{% assign events = site.data.events %}
{% for e in events %}
<div class="card p-3 m-3">
<div class="row">
<div class="col-md-4 text-center"><img src="{{ e.image | prepend: '/objects/' | relative_url }}" alt="{{ e.image_alt }}" class="img-fluid img-thumbnail"></div>
<div class="col-md-8">
<h4>{{ e.title }}</h4>
<p>{{ e.date }}. {{ e.description }}</p>
</div>
</div>
</div>
{% endfor %}
