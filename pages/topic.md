---
layout: page
show_meta: false
title: "議題討論"
subheadline: "公共場所修繕, 設施/設備維修, 門禁管制,環保回收改善..."
header:
   image_fullwidth: "header_unsplash_7.jpg"
permalink: "/topic/"
---

### 住戶提議
* 2024/10/20 **E2-任明仁:** 社區約500個滅火器都是114-06-10到期，明年記得申辦三燈二器，加上火警連動偵測器，緊急照明燈，避難方向指示燈，出口警示燈等，也可省下一筆可觀經費！

---
<ul>
    {% for post in site.categories.topic %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
