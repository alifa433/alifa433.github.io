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
      <figure>
        {% assign credential_link = credential.url | default: credential.profile_url %}
        {% if credential_link %}<a href="{{ credential_link }}" target="_blank" rel="noopener noreferrer">{% endif %}
          <img src="{{ '/images/' | append: credential.image | relative_url }}" alt="{{ credential.alt }}" loading="lazy" width="400" height="400">
        {% if credential_link %}</a>{% endif %}
        <figcaption>
          <h2>{{ credential.name }}</h2>
          <p>{{ credential.category }}{% if credential.issuer %} · {{ credential.issuer }}{% endif %}</p>
        </figcaption>
      </figure>
    </article>
  {% endfor %}
</div>
