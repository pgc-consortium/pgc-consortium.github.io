---
layout: sop
title: Standard Operating Procedures
permalink: /sops/
---


  <!-- SOP page -->
<div class="container">
  <div class="page-head">
    <h1 class="page-title">{{ page.title }}</h1>
    {% if page.description %}
      <p class="page-description">{{ page.description }}</p>
    {% endif %}
  </div>
</div>

<div class="sops-page container animate">
  <div class="row">
    {% for file in site.data.sops %}
      <article class="sop col col-4 col-d-6 col-t-12">
        <div class="sop__content">
          {% if file.image %}
          <a href="/assets/sops/{{ file.filename }}" class="sop__image">
            <img src="{{ file.image }}" alt="{{ file.title }}">
          </a>
          {% endif %}
          <div class="sop__info">
            <h3 class="sop__title">
              <a href="/assets/sops/{{ file.filename }}" download>{{ file.title }}</a>
            </h3>
            {% if file.description %}
            <div class="sop__subtitle">{{ file.description }}</div>
            {% endif %}
            <a href="/assets/sops/{{ file.filename }}" download class="button button--primary button--small">Download</a>
          </div>
        </div>
      </article>
    {% endfor %}
  </div>
</div>