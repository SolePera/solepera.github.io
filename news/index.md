---
title: News
layout: splash
header:
    overlay_filter: "0.2"
    overlay_image: /images/newsHead.jpg
    caption: "Photo by [Patrick Tomasso](https://unsplash.com/@impatrickt?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/s/photos/pages?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)"
---

<div>
{% assign cur = '2101' %}
{% assign sorted = (site.news | sort: 'date') | reverse %}
{% for pub in sorted limit:12 %}
{% capture year %}{{pub.date | date:'%Y'}}{% endcapture %}
{% assign cur = year %}
    <div class="grid-item">
    <a href = "{{ pub.picture }}"> <img src="{{ pub.picture }}" alt="Photo of a {{ pub.title | downcase }}" style="float:left;width:300px;"> </a>
    <a href="{{ pub.link }}">{{ pub.title }}</a>    
    </div>
{% endfor %}

</div>
