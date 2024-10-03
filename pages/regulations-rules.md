---
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
法規名稱：內政部 [公寓大廈管理條例 111-05-11.pdf](https://github.com/coconutcity30050/community27/blob/gh-pages/assets/rules/%E5%85%AC%E5%AF%93%E5%A4%A7%E5%BB%88%E7%AE%A1%E7%90%86%E6%A2%9D%E4%BE%8B111-05-11.pdf)<br>

全國法規資料庫: [公寓大廈管理條例](https://law.moj.gov.tw/LawClass/LawAll.aspx?pcode=D0070118)<br>

---
### AI法條諮詢
<p><img src="https://github.com/coconutcity30050/community27/raw/gh-pages/images/gemini_logo.png"></p>

<h1>Gemini Chatbot</h1>
<div id="chatHistory">
    <!-- Chat history will appear here -->
</div>
<div class="inputs">
    <input type="password" id="apiKey" placeholder="API Key" />
    <input
         type="text"
         id="messageInput"
         placeholder="Type your message here..."
    />
    <button onclick="sendMessage()">Send</button>
</div>
<script>
    const converter = new showdown.Converter();
    let thread = [];
    function sendMessage() {
        var apiKey = document.getElementById("apiKey").value;
        const message = document.getElementById("messageInput").value;
        document.getElementById("chatHistory").innerHTML +=
            "<div><div class='author'>You:</div>" + message + "</div>";
        thread.push({
            role: "user",
            parts: [{ text: message }],
        });
        console.log(apiKey);
        fetch("https://generativelanguage.googleapis.com/v1beta/models/gemini-pro:generateContent?key=" +
                        apiKey,
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


---
## 椰城社區規約
<br>
[椰城社區規約與管理辦法113-05-10.pdf](https://github.com/coconutcity30050/community27/blob/gh-pages/assets/rules/%E6%A4%B0%E5%9F%8E%E7%A4%BE%E5%8D%80%E8%A6%8F%E7%B4%84%E5%8F%8A%E7%AE%A1%E7%90%86%E8%BE%A6%E6%B3%95113-05-10.pdf)<br>


<a class="radius button small" href="{{ site.url }}{{ site.baseurl }}/documentation/">查看本屆社區公告文件 ›</a><br>


 [1]: {{ site.url }}{{ site.baseurl }}/documentation/
