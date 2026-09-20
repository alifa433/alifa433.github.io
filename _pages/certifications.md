---
layout: single
title: "Certifications"
description: "Professional certifications held by Ali Farhani in project management and blockchain fundamentals."
permalink: /certifications/
author_profile: true
---

The following certifications are presented from the original credential images supplied for this website.

<div class="credentials-page">
  {% for credential in site.data.certifications %}
    <article class="credential-card credential-card--page">
      {% assign credential_link = credential.url | default: credential.profile_url %}
      <figure class="credential-card__figure">
        {% if credential_link %}<a class="credential-card__image-link" href="{{ credential_link }}" target="_blank" rel="noopener noreferrer">{% endif %}
          <span class="credential-card__image-frame">
            <img src="{{ '/images/' | append: credential.image | relative_url }}" alt="{{ credential.alt }}" loading="lazy" width="400" height="400">
          </span>
        {% if credential_link %}</a>{% endif %}
        <figcaption>
          <h2>{{ credential.name }}</h2>
          <p>{{ credential.category }}{% if credential.issuer %} · {{ credential.issuer }}{% endif %}</p>
          {% if credential_link %}<a class="credential-card__link" href="{{ credential_link }}" target="_blank" rel="noopener noreferrer">View credential <span aria-hidden="true">↗</span></a>{% endif %}
        </figcaption>
      </figure>
    </article>
  {% endfor %}
</div>
