---
layout: page
show_meta: false
title: "場所與設備"
subheadline: "社區各場所與設備現況"
header:
   image_fullwidth: "header_unsplash_5.jpg"
permalink: "/places/"
---
<ul>
    {% for post in site.categories.places %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
