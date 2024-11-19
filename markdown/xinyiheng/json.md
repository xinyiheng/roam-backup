- 在早期互联网传递数据时主要是通过 [[xml]]文档来进行，而 XML 就跟我们的 HTML 形式类似，其过于啰嗦且繁复。由于前端技术的发展使得 XML 不太能满足开发者快速进行数据传输与交换的需要，于是 一种新型的数据传输格式类型 JSON 就被一个名为 Douglas Crockford 的人所创建。
  
  JSON（[[JavaScript]] Object Notation，即 JavaScript 对象表示法），是一种轻量的^^数据交换格式^^，也和前端 JavaScript 语言的对象语法相契合：
  {
      "site": "https://www.sspai.com",
      "author": "100gle",
      "name": "《Python 自学手册》"
  }
  如果你反应足够快的话，可能就知道这东西和 Python 里内置的[[字典]]类型长得十分像。
  via[附加案例二：用于获取数据的爬虫 - 少数派](https://sspai.com/post/63900)
  [[20201225]] 上午9:03
- json在[[爬虫]]中的使用
    - 如果我们能直接获取到对应的[[API]]返回的 JSON 数据，那么就不需要再使用什么正则或者选择器去挖出对应的数据部分，我们直接就能拿着 JSON 到程序中进行解析，并获取对应键值对即可。
      
      一般接口请求的响应结果我们也可以直接在开发者工具控制台中的 Network 网络选项卡中看到（需要我们重新刷新网页）。然后点击 XHR 选项卡就可以看到请求的接口信息：
      via[附加案例二：用于获取数据的爬虫 - 少数派](https://sspai.com/post/63900)
      [[20201225]] 上午9:05
    - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FyAsVK06qxs.png?alt=media&token=f12e2428-92d1-45f1-9553-4d3593b5c901)
- [手把手教你用飞书 Webhook 打造一个消息推送 Bot - 少数派](https://sspai.com/post/68578)
    - 什么是 JSON？JSON（JavaScript Object Notation，即 JavaScript 对象表示法），是目前在 Web 领域里被广泛用于数据传递与交换的文件格式之一。JSON 通常由键值对构成，就像这样： { "id": 1, "name": "100gle", "site": "https://sspai.com/u/100gle/posts", "social_media": ["sspai", "Github"], "product": { "name": "Python 自学手册", "url": "https://sspai.com/series/148/list" } } 而我们的消息也是需要以这种格式来发送，当中包含的是关于该消息的类型、内容、其他参数等信息。
    - 什么是 JSON？JSON（JavaScript Object Notation，即 JavaScript 对象表示法），是目前在 Web 领域里被广泛用于数据传递与交换的文件格式之一。JSON 通常由键值对构成，就像这样：
    - { "id": 1, "name": "100gle", "site": "https://sspai.com/u/100gle/posts", "social_media": ["sspai", "Github"], "product": { "name": "Python 自学手册", "url": "https://sspai.com/series/148/list" } }
    - 而我们的消息也是需要以这种格式来发送，当中包含的是关于该消息的类型、内容、其他参数等信息。
