---
layout: page
subheadline: "Header"
title: "Style your Header!"
teaser: "header image is 16:9, the width should be 1600 pixels"
header:
   image_fullwidth: "header_unsplash_5.jpg"
permalink: "/headers/"
---
<ul>
    {% for post in site.tags.header %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
