---
title: Latest Publications
layout: single
toc: true
header:
    overlay_image: /images/header-bg-nopic.jpg

---

{% assign cur = '2101' %}
{% for pub in site.pubs reversed %}
{% capture year %}{{pub.date | date:'%Y'}}{% endcapture %}
{% if year != cur %}## {{year}} {% endif %}
{% assign cur = year %}
{{pub.excerpt | replace: "#", pub.url }}
{% endfor %}
