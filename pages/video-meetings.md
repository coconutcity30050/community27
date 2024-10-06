---
layout: page
subheadline: "Video Meetings"
title: "管委會會議"
teaser: "第27屆管委會 會議直播影片"
header:
   image_fullwidth: "header_unsplash_5.jpg"
permalink: "/video-meetings/"
---

<ul>
    {% for post in site.tags.meeting %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>

