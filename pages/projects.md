---
title: Digital Projects
layout: page
permalink: /projects/
---

# Digital Projects 

Digital projects related to Company Town Legacy created by University of Idaho students.

<div class="row">
{% assign projects = site.data.digital_projects %}
{% for p in projects %}
<div class="item col-md-4 mb-2" >
    <div class="card">
        <a href="{{ p.link }}" target="_blank">
            <img class="card-img-top lazy" src="{{ p.thumbnail | prepend: '/objects/' | relative_url }}" alt="{{ p.thumb_caption }}">
        </a>
        <div class="card-body text-center search">
            <h3 class="card-title">{{ p.title }}</h3>
            <p class="card-text">{{ p.description }}</p>
            <p class="card-text">{{ p.creator }}, {{ p.date }}.</p>
            <p>
                <a href="{{ p.link }}" target="_blank" class="btn btn-sm btn-outline-info" title="link to {{ p.title | escape }}">View Project</a>
            </p>
        </div>
    </div>
</div>
{% endfor %}
</div>