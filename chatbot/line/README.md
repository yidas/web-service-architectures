LINE BOT
========

API Flow
--------

### Message Reply

<img src="https://raw.githubusercontent.com/yidas/web-service-architectures/master/chatbot/line/api-flow.png" />

- Above example is a simple implementation for Line webhook quick reply, which sends reply requests during webhook request.

- For a same Line user, there is a message queue mechanism to guarantee the reply sequence. A previous webhook with messages will lock the subsequent webhook's replies until the previous webhook getting response.

---

Web View Auth application scenario
-------------

If you would like to implement authentication in LINE Webview without using [LIFF](https://developers.line.biz/en/docs/liff/overview/):

<img src="https://raw.githubusercontent.com/yidas/web-service-architectures/master/chatbot/line/chatbot-line-webview.png" />

> Event hook from LINE should bring the user channelId for authentication bundling.

