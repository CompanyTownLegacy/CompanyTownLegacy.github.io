---
title: Oral Histories
layout: page
permalink: /histories/
---

# Oral Histories 

A selection of oral histories related to Company Town Legacy.

<div class="row">
{% assign histories = site.data.companytownlegacy_oralhistories %}
{% for h in histories %}
<div class="item col-md-4 mb-2" >
    <div class="card">
        <div class="card-body text-center search">
            <h3 class="card-title">{{ h.title }}</h3>
            <img class="img-fluid p-3" src="{{ h.thumbnail | prepend: '/objects/' | relative_url }}" alt="{{ p.thumb_caption }}">
            <p class="card-text">{{ h.description }} ({{ h.date }})</p>
            <p>
                <button class="btn btn-info" title="{{ h.title | escape }}" type="button" data-toggle="modal" data-target="#modal{{ h.indexid }}">View Video</button>
            </p>
        </div>
    </div>
    <!-- modal -->
    <div class="modal fade" id="modal{{ h.indexid }}" tabindex="-1" role="dialog" aria-labelledby="modalTitle{{ h.indexid }}" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered modal-lg" role="document">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="modalTitle{{ h.indexid }}">{{ h.title }}</h5>
                    <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                        <span aria-hidden="true">&times;</span>
                    </button>
                </div>
                <div class="modal-body">
                    <div class="embed-responsive embed-responsive-16by9">
                        <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/{{ h.youtubeid }}?rel=0" allowfullscreen></iframe>
                        </div>
                    <p>{{ h.description }}</p>
                </div>
            </div>
        </div>
    </div>
</div>
{% endfor %}
</div>
