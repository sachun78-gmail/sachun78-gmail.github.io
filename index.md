---
layout: default
title: 포트폴리오
---

## About

{% for line in site.data.profile.summary %}
- {{ line }}
{% endfor %}

## Skills

<div class="chips">
  {% for skill in site.data.profile.skills %}
    <span class="chip">{{ skill }}</span>
  {% endfor %}
</div>

## Projects

{% for p in site.data.projects %}
<section class="card">
  <h3>{{ p.id }}. {{ p.title }} <small>{{ p.subtitle }}</small></h3>
  <p class="meta"><strong>기간:</strong> {{ p.period }} · <strong>인원:</strong> {{ p.team }} · <strong>역할:</strong> {{ p.role }}</p>
  {% if p.site_url %}
  <p><strong>서비스 링크:</strong> <a href="{{ p.site_url }}" target="_blank" rel="noopener noreferrer">{{ p.site_url }}</a></p>
  {% endif %}
  <p><strong>개요:</strong> {{ p.overview }}</p>

  {% if p.tech_stack %}
  <p><strong>기술 스택:</strong></p>
  <ul>
    {% for t in p.tech_stack %}
    <li>{{ t }}</li>
    {% endfor %}
  </ul>
  {% endif %}

  {% if p.architecture %}
  <p><strong>아키텍처:</strong></p>
  <ul>
    {% for a in p.architecture %}
    <li>{{ a }}</li>
    {% endfor %}
  </ul>
  {% endif %}

  {% if p.key_features %}
  <p><strong>주요 기능:</strong></p>
  <ul>
    {% for f in p.key_features %}
    <li>{{ f }}</li>
    {% endfor %}
  </ul>
  {% endif %}

  {% if p.implementation %}
  <p><strong>핵심 구현:</strong></p>
  <ul>
    {% for i in p.implementation %}
    <li>{{ i }}</li>
    {% endfor %}
  </ul>
  {% endif %}

  {% if p.key_contributions %}
  <p><strong>주요 기여:</strong></p>
  <ul>
    {% for c in p.key_contributions %}
    <li>{{ c }}</li>
    {% endfor %}
  </ul>
  {% endif %}

  {% if p.troubleshooting %}
  <p><strong>트러블슈팅:</strong></p>
  <ul>
    {% for tr in p.troubleshooting %}
    <li>{{ tr }}</li>
    {% endfor %}
  </ul>
  {% endif %}
</section>
{% endfor %}

## Core Competencies

{% for c in site.data.profile.core_competencies %}
### {{ c.title }}
{% for item in c.items %}
- {{ item }}
{% endfor %}
{% endfor %}
