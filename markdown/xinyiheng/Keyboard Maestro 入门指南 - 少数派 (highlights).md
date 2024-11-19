- Author:: [[sspai.com]]
- Full Title:: Keyboard Maestro 入门指南 - 少数派
- Category:: #articles
- Document Tags:: #[[工具]]
- URL:: https://sspai.com/post/36442
- ### Highlights first synced by #Readwise [[March 10th, 2023]]
    - ### 通过 Alfred 或 LaunchBar 来启动 Macro
      
      
      并不是所有的 Macro 都需要设定一个触发器，有时候可以把他放在 MenuBar 中的 Keyboard Maestro Engine 中来启动，或者干脆只通过 [Alfred](tag/Alfred) 或 [LaunchBar](tag/LaunchBar) 来启动。
    - #### 取代 TextExpander
      
      
      [TextExpander](tag/TextExpander) 在升级到版本 6 以后，收费方式从一次买断转变成了订阅制：个人用户年付 40 美元，团队用户年付 95 美元，价格大幅上升的同时功能上却并没有实质提升，有充足的理由使用 Keyboard Maestro 来代替他。
      
      
      以把剪贴板中的 URL 转换成 MarkDown 格式并插入为例：
      
      
      可以使用 `Typed String Trigger`，当按下预设的关键字：`[][]`时，就会自动扩展并将剪贴板粘贴内容和光标都放到对应的位置。
