---
title: News
layout: splash
header:
    overlay_image: /images/header-bg-nopic.jpg
#%    overlay_filter: "0.2"
#%    overlay_image: /images/newsHead.jpg
#%    caption: "Photo by [Patrick Tomasso](https://unsplash.com/@impatrickt?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/s/photos/pages?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)"
---

<table class="grid-container">
{% assign cur = '2101' %}
{% assign sorted = (site.news | sort: 'date') | reverse %}
{% tablerow pub in sorted cols:3 limit:15 %}
{% capture year %}{{pub.date | date:'%Y'}}{% endcapture %}
{% assign cur = year %}
    <div class="grid-item">
        <a href = "{{ pub.picture }}"> <img src="{{ pub.picture }}" alt="Photo of a {{ pub.title | downcase }}" style="width:300px;height:300px;object-fit:contain;"></a>
        <br>
        <a class="pub-title" href="{{ pub.link }}">{{ pub.title }}</a>
    </div>
{% endtablerow %}
</table>
