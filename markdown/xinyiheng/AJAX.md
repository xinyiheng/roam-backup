- **AJAX** 的全称是 **Asynchronous JavaScript and XML（异步的 JavaScript 和 XML）**，是前端开发中一个非常核心的技术概念，简单说，它的作用是：
    - **在不刷新整个网页的情况下，向服务器发送请求并获取数据。**
- ### 举个例子：
    - 比如你打开一个网页，点击“加载更多”按钮，页面没有跳转，但新内容加载出来了——这就是 AJAX 的功劳。
- ### AJAX 能做什么？
    - 提交表单而不刷新页面
    - 搜索框联想（输入时自动补全）
    - 动态刷新评论、点赞数量等数据
    - 实时与后端通信（如聊天室）
- ### 技术核心：
    - AJAX 不是一门新语言，而是一种使用现有技术的“组合”方式，核心包括：
        - **JavaScript**：写逻辑
        - **XMLHttpRequest 或 Fetch API**：与服务器通信
        - **JSON**（现代常用）或 XML：传输数据格式
        - **HTML / CSS**：动态更新页面内容
- ### 示例（使用 `fetch` 实现 AJAX 请求）：
    - ```javascript
      javascriptCopyEditfetch('https://api.example.com/data')
        .then(response => response.json())
        .then(data => {
          console.log(data); // 处理返回的数据
        });
      ```
