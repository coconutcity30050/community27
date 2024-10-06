---
layout: page
subheadline: "Finance Report"
title: "財務報表"
teaser: "第27屆管委會任期 113年10月~114年10月"
header:
   image_fullwidth: "header_unsplash_5.jpg"
permalink: "/headers/"
---

椰城規約第十七條 管理委員會之會計年度自當年 11 月 01 日起至次年 10 月 31 日止。<br>

<ul>
    {% for post in site.tags.header %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
