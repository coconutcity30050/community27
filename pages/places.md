---
layout: page
show_meta: false
title: "場所與設備"
subheadline: "社區各場所與設備現況"
header:
   image_fullwidth: "header_unsplash_5.jpg"
permalink: "/places/"
---

## 社區門牌號碼對照圖

![](https://github.com/coconutcity30050/community27/raw/gh-pages/images/%E6%A4%B0%E5%9F%8E%E7%A4%BE%E5%8D%80%E9%96%80%E7%89%8C%E6%88%B6%E8%99%9F%E5%B0%8D%E7%85%A7%E8%A1%A8.jpg)

<ul>
    {% for post in site.categories.places %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
