---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: header_unsplash_12.jpg
  
widget1:
  title: "管委會之會議議程"
  url: 'https://coconutcity30050.github.io/community27/committee/'
  image: widget-1-302x182.jpg
  text: '
  <em>10/17已完成管理委員選舉</em><br/><br/>
  <u>10/29 8:00pm 完成管理委員互選</u><br/>
  <u>11/01 第27屆管理委員正式上任</u><br/>
  <u>11/12 7:30pm~8:30pm 11月第一次會議</u><br/>
  '
  
widget2:
  title: "第27屆之政見與任務"
  url: 'https://coconutcity30050.github.io/community27/info/'
  text: '
  CoconutCity 30050<br/>
  1. 建構<a href="http://github.com/coconutcity30050">椰城社區網頁</a><br/>
  2. 架設<a href="https://studio.youtube.com/channel/UCWDGBuGMQvoysG398_kcrhw/content/posts">社區雲端論壇</a><br/>
  3. 評估社區修繕事項<br/>
  4. 增訂選舉管理辦法<br/>
  5. 增訂採購管理辦法<br/>
  6. 討論垃圾回收改善<br/>
  7. 召集社區志工小組<br/>
  '
  video: '<a href="#" data-reveal-id="videoModal"><img src="https://github.com/coconutcity30050/community27/raw/gh-pages/images/coconutcity30050-nightview-video-459x258.png" width="302" height="182" alt=""/></a>'

widget3:
  title: "管委會之使命與願景"
  url: 'https://coconutcity30050.github.io/community27/'
  image: widget-github-303x182.jpg  
  text: '<em>公開透明社區資訊, 科技化管理制度, 創新社區服務</em><br/>
  <br/>
  Q4`24 評估修繕與排序, 增訂委員選舉管理辦法, 討論垃圾回收改善, 完成郵寄存證信函至欠繳住戶<br/>
  <br/>
  Q1`25 完成預算內之社區修繕, 增訂採購管理辦法, 完成臨時區權會決議與投票, 進行社區合約審議<br/>
  <br/>
  Q2`25 完成保全/物業, 社區清潔之合約簽訂<br/>
  <br/>
  Q3`25 完成區權會決議及第28屆管理委員選舉投票<br/>
  '
   
#
# Use the call for action to show a button on the frontpage
#
# To style the button in different colors, use no value
# to use the main color or success, alert or secondary.
# To change colors see sass/_01_settings_colors.scss
#
callforaction:
  url: https://coconutcity30050.github.io/community27
  text: 社區論議題討論
  style: alert
permalink: /index.html
#
#
homepage: true
---

<p>
<img src="https://github.com/coconutcity30050/community27/raw/gh-pages/assets/img/websiteQR.png">
<img src="https://github.com/coconutcity30050/community27/raw/gh-pages/assets/img/circleQR.png">
</p>

<div id="videoModal" class="reveal-modal large" data-reveal="">
  <div class="flex-video widescreen vimeo" style="display: block;">
    <iframe width="925" height="520" src="https://www.youtube.com/embed/Z7l5DZwq85g" title="椰城之夜 (feat. 新竹椰城社區~E棟頂樓)" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
  </div>
  <a class="close-reveal-modal">&#215;</a>
</div>
