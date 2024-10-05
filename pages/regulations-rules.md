![image](https://github.com/user-attachments/assets/73df3911-399d-4bdf-aa55-57a6fc4ea80a)---
layout              : page
show_meta           : false
title               : "法規 ＆ 規約"
subheadline         : "恪守規約, 戶戶有責"
teaser              : "社區規約是公寓大廈管理組織成立與運作的依據，也是規範住戶權利義務關係的重要依據"
header:
   image_fullwidth  : "header_homepage_13.jpg"
permalink           : "/regulations-rules/"
---
---
## 公寓大廈管理條例
<br>
[內政部公寓大廈管理條例網頁](https://law.moj.gov.tw/LawClass/LawAll.aspx?pcode=D0070118),&nbsp;&nbsp;&nbsp;&nbsp;[公寓大廈管理條例111-05-11.pdf](https://github.com/coconutcity30050/community27/blob/gh-pages/assets/rules/%E5%85%AC%E5%AF%93%E5%A4%A7%E5%BB%88%E7%AE%A1%E7%90%86%E6%A2%9D%E4%BE%8B111-05-11.pdf) <br>

---
## 椰城社區規約
<br>
[椰城社區規約與管理辦法113-05-10.pdf](https://github.com/coconutcity30050/community27/blob/gh-pages/assets/rules/%E6%A4%B0%E5%9F%8E%E7%A4%BE%E5%8D%80%E8%A6%8F%E7%B4%84%E5%8F%8A%E7%AE%A1%E7%90%86%E8%BE%A6%E6%B3%95113-05-10.pdf)<br>

---
## 社區聊天機器人
*目前僅提供普通問答功能, 尚無法提供查詢功能！*<br>

<p><img src="https://github.com/coconutcity30050/community27/raw/gh-pages/images/gemini_logo.png"></p>

<script src="https://cdn.jsdelivr.net/npm/showdown@2.1.0/dist/showdown.min.js"></script>
<style>
    * {
        padding: 0;
        margin: 0;
        box-sizing: border-box;
    }
    body {
        font-family: system-ui, -apple-system, BlinkMacSystemFont,
            "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, "Open Sans",
            "Helvetica Neue", sans-serif;
        padding: 2rem;
        display: flex;
        flex-direction: column;
        height: 100dvh;
    }
    #chatHistory {
        flex-grow: 1;
    }
    .inputs {
        display: flex;
    }
    #messageInput {
    }
    .inputs > * {
        height: 2rem;
        padding: 0.5rem;
    }
    #chatHistory > div {
        margin-top: 1rem;
    }
</style>

<div id="chatHistory">
    <!-- Chat history will appear here -->
</div>

<div class="inputs">
    <input type="text" id="messageInput" placeholder="請於此處輸入您的問題,我將盡力回答您！"/>
    <button onclick="sendMessage()">送出</button>
</div>
<button onclick="clearMesage()">清除</button>

<script>
    const converter = new showdown.Converter();
    let thread = [];
    function clearMessage() {
        document.getElementById("chatHistory").innerHTML = " ";
    }
    function sendMessage() {
        /*var apiKey = document.getElementById("apiKey").value;*/
        var apiKey = "AIzaSyBfva4fTk8OaZnlDdvN_zaXaey0MrezCFo";
        var reg_url = "https://github.com/coconutcity30050/community27/blob/gh-pages/assets/rules/%E5%85%AC%E5%AF%93%E5%A4%A7%E5%BB%88%E7%AE%A1%E7%90%86%E6%A2%9D%E4%BE%8B111-05-11.pdf";
        var rules_url = "https://github.com/coconutcity30050/community27/blob/gh-pages/assets/rules/%E6%A4%B0%E5%9F%8E%E7%A4%BE%E5%8D%80%E8%A6%8F%E7%B4%84%E5%8F%8A%E7%AE%A1%E7%90%86%E8%BE%A6%E6%B3%95113-05-10.pdf";
        const message = document.getElementById("messageInput").value;
        document.getElementById("chatHistory").innerHTML +=
            "<div><div class='author'>You:</div>" + message + "</div>";
        thread.push({
            role: "user",
            parts: [{ text: message }],
        });
        console.log(apiKey);
        fetch("https://generativelanguage.googleapis.com/v1beta/models/gemini-1.5-flash-latest:generateContent?key=" + apiKey,
                    {
                        method: "POST",
                        headers: {
                            "Content-Type": "application/json",
                        },
                        body: JSON.stringify({
                            contents: thread,
                        }),
                    }
                )
                .then(response => response.json())
                .then(data => {
                    const msg = data.candidates[0].content.parts[0].text;
                    document.getElementById("chatHistory").innerHTML +=
                        "<div><div class='author'>Bot:</div>" +
                        converter.makeHtml(msg) +
                        "</div>";
                    thread.push({
                        role: "model",
                        parts: [
                            {
                                text: msg,
                            },
                        ],
                    });
                })
                .catch(error => {
                    console.error("Error:", error);
                    document.getElementById("chatHistory").innerHTML +=
                        "<div><div class='author'>Bot:</div>Error: " +
                        error +
                        "</div>";
                });
        }
</script>

<a class="radius button small" href="{{ site.url }}{{ site.baseurl }}/documentation/">查看本屆社區公告文件 ›</a><br>


 [1]: {{ site.url }}{{ site.baseurl }}/documentation/