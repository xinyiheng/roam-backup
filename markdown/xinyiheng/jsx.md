- JSX 是 **JavaScript XML** 的缩写，是 React 中常用的一种语法扩展。
- 简单来说：**JSX 让你可以在 JavaScript 代码里像写 HTML 一样写界面元素。**
- ### 🔍 举个例子
    - **普通 JavaScript：**
    - ```javascript
      const element = React.createElement('h1', null, 'Hello, world!');
      ```
    - **用 JSX 写：**
    - ```javascript
      const element = <h1>Hello, world!</h1>;
      ```
    - 这两段代码最终的效果完全一样，但后者（JSX）看起来更直观、简洁。
- ### 🧠 本质上：
    - JSX 并不是浏览器原生支持的语法。它是 **React 提供的一种语法糖**，在打包构建过程中（比如用 Vite、Webpack）会被 **Babel 编译**成标准的 `React.createElement(...)` 调用。
- ### 🧩 JSX 能做什么？
    - 你可以在 JSX 中：
        - 像写 HTML 一样写组件结构
        - 在标签中插入变量：`{title}`
        - 嵌套表达式、条件渲染、循环渲染等
    - 例子：
    - ```javascript
      function Welcome(props) {
        return <h1>Hello, {props.name}</h1>;
      }
      ```
- ### ⚠️ JSX 和 HTML 的不同点：
    - 虽然看起来像 HTML，其实有些规则是不同的，比如：
    - {{[[table]]}}
        - HTML
            - JSX
        - `class`
            - `className`
        - `for`
            - `htmlFor`
        - 属性必须闭合
            - `<img />`
        - 样式用对象
            - `style={{ color: 'red' }}`
