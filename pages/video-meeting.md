---
layout: page
subheadline: "Video Meeting"
title: "社區管委會會議"
teaser: "第27屆管委會會議 YouTube直播"
header:
   image_fullwidth: "header_unsplash_5.jpg"
permalink: "/video-meeting/"
---

<ul>
    {% for post in site.tags.meeting %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>

