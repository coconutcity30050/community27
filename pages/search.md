---
permalink: /search/
layout: page
title: "Search"
sitemap: false
---

{% include _google_search.html %}

---
### Chatbot
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
    <button onclick="sendMessage()">Send</button>
</div>

<script>
    const converter = new showdown.Converter();
    let thread = [];
    function sendMessage() {
        /*var apiKey = document.getElementById("apiKey").value;*/
        var apiKey = "AIzaSyBfva4fTk8OaZnlDdvN_zaXaey0MrezCFo";
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
