---
layout: about
title: about
permalink: /
subtitle: >
  Computer Vision Engineer at <a href="https://www.stradvision.com/">StradVision</a> ·
  M.S. Mechanical Engineering, Seoul National University

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false
  more_info: >
    <p>Seoul, Korea</p>
    <p><a href="mailto:hasunlee@snu.ac.kr">hasunlee@snu.ac.kr</a></p>

selected_papers: true
social: true

announcements:
  enabled: false

latest_posts:
  enabled: true
  scrollable: true
  limit: 3
---

I am a computer vision engineer at [StradVision](https://www.stradvision.com/), working on 3D perception for multi-fisheye automotive cameras and production ADAS features. I received my M.S. in Mechanical Engineering from [Seoul National University](https://www.snu.ac.kr/) (INRoL) and my B.S. in Physics from [POSTECH](https://www.postech.ac.kr/).

{% assign career = site.data.career %}
{% if career %}

<style>
  .career-timeline {
    margin: 2.5rem 0 1rem;
  }

  .career-timeline h2 {
    font-size: 1.35rem;
    font-weight: 600;
    margin: 0 0 1.25rem;
  }

  .career-timeline-list {
    list-style: none;
    margin: 0;
    padding: 0 0 0 0.25rem;
    position: relative;
  }

  .career-timeline-item {
    display: grid;
    grid-template-columns: 2.5rem 1fr;
    gap: 0 1rem;
    padding-bottom: 1.75rem;
    position: relative;
  }

  .career-timeline-item:last-child {
    padding-bottom: 0;
  }

  .career-timeline-item:not(:last-child)::before {
    background: color-mix(in srgb, currentColor 18%, transparent);
    bottom: 0;
    content: "";
    left: 1.2rem;
    position: absolute;
    top: 2.6rem;
    width: 2px;
  }

  .career-timeline-icon {
    align-items: center;
    background: color-mix(in srgb, var(--global-theme-color, #2698ba) 16%, transparent);
    border: 1px solid color-mix(in srgb, var(--global-theme-color, #2698ba) 35%, transparent);
    border-radius: 999px;
    color: var(--global-theme-color, #2698ba);
    display: inline-flex;
    height: 2.4rem;
    justify-content: center;
    position: relative;
    width: 2.4rem;
    z-index: 1;
  }

  .career-timeline-content {
    min-width: 0;
    padding-top: 0.15rem;
  }

  .career-timeline-title {
    font-size: 1rem;
    font-weight: 600;
    line-height: 1.35;
    margin: 0 0 0.2rem;
  }

  .career-timeline-org {
    color: color-mix(in srgb, currentColor 72%, transparent);
    font-size: 0.95rem;
    line-height: 1.4;
    margin: 0 0 0.15rem;
  }

  .career-timeline-org a {
    color: inherit;
    text-decoration: none;
  }

  .career-timeline-org a:hover {
    color: var(--global-theme-color, #2698ba);
    text-decoration: underline;
  }

  .career-timeline-meta,
  .career-timeline-detail {
    color: color-mix(in srgb, currentColor 58%, transparent);
    font-size: 0.9rem;
    line-height: 1.4;
    margin: 0;
  }

  .career-timeline-detail {
    margin-top: 0.15rem;
  }

  .career-timeline-heading-spaced {
    margin-top: 2rem;
  }
</style>

<section class="career-timeline" aria-label="Career timeline">
  {% if career.experience.size > 0 %}
    <h2>Experience</h2>
    <ol class="career-timeline-list">
      {% for item in career.experience %}
        <li class="career-timeline-item">
          <span class="career-timeline-icon" aria-hidden="true"><i class="fa-solid fa-briefcase"></i></span>
          <div class="career-timeline-content">
            <p class="career-timeline-title">{{ item.role }}</p>
            <p class="career-timeline-org">
              {% if item.url %}
                <a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">{{ item.organization }}</a>
              {% else %}
                {{ item.organization }}
              {% endif %}
            </p>
            <p class="career-timeline-meta">{{ item.start }} – {{ item.end }}</p>
          </div>
        </li>
      {% endfor %}
    </ol>
  {% endif %}

{% if career.education.size > 0 %}
<h2{% if career.experience.size > 0 %} class="career-timeline-heading-spaced"{% endif %}>Education</h2>

<ol class="career-timeline-list">
{% for item in career.education %}
<li class="career-timeline-item">
<span class="career-timeline-icon" aria-hidden="true"><i class="fa-solid fa-graduation-cap"></i></span>
<div class="career-timeline-content">
<p class="career-timeline-title">{{ item.degree }}</p>
<p class="career-timeline-org">
{% if item.url %}
<a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">{{ item.institution }}</a>
{% else %}
{{ item.institution }}
{% endif %}
</p>
<p class="career-timeline-meta">{{ item.start }} – {{ item.end }}</p>
{% if item.detail %}
<p class="career-timeline-detail">{{ item.detail }}</p>
{% endif %}
</div>
</li>
{% endfor %}
</ol>
{% endif %}

</section>
{% endif %}
