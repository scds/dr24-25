---
layout: home
title: Home
nav_order: 1
---

{%- assign workshops = site.pages 
    | where_exp: "item", "item.grand_parent == null"
    | where_exp: "item", "item.parent == null"
    | sort: "title" 
-%}

<img src="assets/img/titleSlide.png" alt="Workshop Title Slide" width="100%">

# 2024-2025 Digital Research Workshops

Launched in 2023-2024, Digital Research workshops draw on the expertise of colleagues in the Digital Research Commons Pilot, including the Research Software Development team. Digital Research workshops help registrants with information security, website development, code management, and research impact.

These workshops welcome students, staff, and faculty from any discipline, as well as the public at large. Some are also geared towards beginners, so even if you’re new to digital research, we encourage you to sign up and learn!

## 2024-25 DR Workshops     

<div markdown="1" style="border: 1px solid #7a003c; border-radius: 6px; margin-bottom: 1em; padding: 0.5em 1em 0; margin-top: 1em;" class="toc">
<summary style="cursor:default; display: block; border-bottom: 1px solid #302d36; margin-bottom: 0.5em">
  Workshops
</summary>
<ul>
{% for workshop in workshops %}
  {% if workshop.title != null and workshop.title != "Home" %}
<li><a href="{{workshop.url | absolute_url}}">{{workshop.title}}</a></li>
  {% endif %}
{% endfor %}
</ul>
</div>