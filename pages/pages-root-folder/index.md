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
  title: "管委會成員與職掌"
  url: 'http://coconutcity30050.github.io/community27/blog/'
  image: widget-1-302x182.jpg
  text: 'Cominig Soon...'
  
widget2:
  title: "第27屆之政見與任務"
  url: 'http://coconutcity30050.github.io/community27/info/'
  text: '<em>CoconutCityy 30050</em><br/>
  1. 建構<a href="http://github.com/coconutcity30050">椰城社區網頁</a><br/>
  2. 架設<a href="https://studio.youtube.com/channel/UCWDGBuGMQvoysG398_kcrhw/content/posts">社區雲端論壇</a><br/>
  3. 全面評估社區修繕事項<br/>
  4. 革新工程採購制度<br/> 
  5. 優化事務管理,制定規約落實制度<br/>
  6. 建置財務查詢系統<br/>
  7. 建立社區志工小組<br/>'
  video: '<a href="#" data-reveal-id="videoModal"><img src="https://github.com/coconutcity30050/community27/blob/gh-pages/images/coconutcity30050-nightview-video-459x258.png?raw=true" width="302" height="182" alt=""/></a>'
  
widget3:
  title: "管委會之使命與願景"
  url: 'https://github.com/coconutcity30050/community27'
  image: widget-github-303x182.jpg
  text: '<em>資訊公開透明, 制度科技化管理, 社區創新服務, 快樂分享生活'
  
#
# Use the call for action to show a button on the frontpage
#
# To make internal links, just use a permalink like this
# url: /getting-started/
#
# To style the button in different colors, use no value
# to use the main color or success, alert or secondary.
# To change colors see sass/_01_settings_colors.scss
#
callforaction:
  url: https://tinyletter.com/feeling-responsive
  text: Inform me about new updates and features ›
  style: alert
permalink: /index.html
#
#
homepage: true
---

<div id="videoModal" class="reveal-modal large" data-reveal="">
  <div class="flex-video widescreen vimeo" style="display: block;">
    <iframe width="925" height="520" src="https://www.youtube.com/embed/Z7l5DZwq85g" title="椰城之夜 (feat. 新竹椰城社區~E棟頂樓)" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
  </div>
  <a class="close-reveal-modal">&#215;</a>
</div>
