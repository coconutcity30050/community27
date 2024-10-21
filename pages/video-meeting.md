---
layout: page
subheadline: "Video Meeting"
title: "管理委員會議"
teaser: "第27屆管委會會議 YouTube直播"
header:
   image_fullwidth: "header_unsplash_3.jpg"
permalink: "/video-meeting/"
---

### 會議記錄

---
### 直播影片
<ul>
    {% for post in site.tags.meeting %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>

