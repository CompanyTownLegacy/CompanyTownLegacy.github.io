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
<div class="card my-3"><div class="card-body">
<div class="row">
    {% if p.img %}<div class="col-md-2 text-center">
        <img src="{{ p.img | prepend: '/objects/' | relative_url }}" alt="photo of {{ p.name | escape }}" class="img-fluid rounded">
    </div>{% endif %}
    <div class="col-md-10">
        <strong>{{ p.name }}</strong><br>
        <em>{{ p.affiliation }}</em><br>
        {{ p.bio }}
    </div>
</div>
</div></div>
{% endfor %}
