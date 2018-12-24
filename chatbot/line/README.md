Line BOT
========

API Flow
--------

<img src="https://raw.githubusercontent.com/yidas/web-service-architectures/master/chatbot/line/api-flow.png" />

- For a same Line user, there is a message queue mechanism to guarantee the reply sequence. A previous webhook with messages will lock the subsequent webhook's replies until the previous webhook getting response.

---

Web View Auth
-------------

<img src="https://raw.githubusercontent.com/yidas/web-service-architectures/master/chatbot/line/chatbot-line-webview.png" />
