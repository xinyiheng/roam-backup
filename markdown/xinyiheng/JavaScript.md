- roam之类的网页应用很多互动效果是通过javascript实现的。能够支持javascrpt的笔记工具应该可以实现更多的互动性。
-  Marginnote3.6.7推出插件系统后，不仅官方可以在不影响主程序的基础上为用户定制功能，懂javascript的用户也可以自由发挥，编写自己的独属插件。这会给应用带来更多的可能性，anki丰富的插件生态就是一个很好的例子。  [bbs.marginnote.cn](https://bbs.marginnote.cn/t/topic/6246/1)
- javascript
    - [油猴使用指南 01：传说中的「油猴」与用户脚本 - 少数派](https://sspai.com/post/68574)
        - 用户脚本其实是一种注入式的 JavaScript 程序，在网页本身的程序之外，通过一些手段，将用户需要的数据和逻辑注入到当前的网页中，达到修改界面、增加功能等等的目的。
        - 换句话说用户脚本也是 JavaScript。JavaScript 能实现的能力，用户脚本基本也能做，比如操作页面元素，可以给页面中增加、删减、修改页面元素，最常见的去广告脚本就是这么实现的。
        - 用户脚本能提供一些普通 JavaScript 实现不了的能力。Greasymonkey 在最早的 0.25 版本中就带来了两个基本的功能： GM_xmlhttpRequest：用于发起跨域请求GM_registerMenuCommand：当用户操作菜单时，触发一个行为
        - 除了这两个功能之外，目前的用户脚本，大多采用了 Greasemonkey 制定的 [V4 API 规范](https://wiki.greasespot.net/Greasemonkey_Manual:API)。通过这个规范，我们就能知道用户脚本可以做什么了。 本地存储数据：这个能力和浏览器自带的 localStorage 比较像，可以给予用户脚本存储一些数据的能力。比如一些个性化的用户设置（譬如一张可爱的背景图）、用户数据（你关注的股票和基金）等等。获取外部资源：譬如从外部的地址获取图片、CSS 文件等等。发起浏览器提醒：调用浏览器右上角的那种提醒，可以指定文字图片和点击之后的效果。打开一个新页面：这个就很好理解，就是打开一个新的页面……设置剪贴板：这个能力可以访问你的剪贴板并给里面塞进去指定的内容。在 V3 版本的 API 中，还多了几个能力，包括： 插入 CSS 样式下载文件
        - 当然我更推荐下面的几个脚本源： [GreasyFork](https://greasyfork.org/) 可能是目前量最大的源，最开始让大家体验的 [少数派作者激励器](https://wvsjslugj8.feishu.cn/docs/%28https://greasyfork.org/zh-CN/scripts/429067-%E5%B0%91%E6%95%B0%E6%B4%BE%E4%BD%9C%E8%80%85%E6%BF%80%E5%8A%B1%E5%99%A8)也是这个平台中托管的[OpenUserJS](https://openuserjs.org/) 另一个开放的脚本源[Userscript.Zone](https://www.userscript.zone/)当然，直接在 GitHub 上去找脚本也是个不错的选择。
        - 因此我自己的解决方案是，对于轻量一些的场景，通过用户脚本+用户样式（user style）解决大部分浏览需求，重一些的场景则会选择浏览器扩展。
        - 用户脚本作为一个 17 年前的互联网老古董，现如今仍有自己的用武之地，还是十分令人感慨。但作为油猴使用指南的第一期，本文仅为增加大家对「油猴脚本」的一点了解，如果你想解锁用户脚本的全部实力、甚至自己动手制作用户脚本，还请留意本系列的后续内容更新。
    - [javascript](https://www.zhihu.com/search?type=content&q=javascript)学习
        - Javascript 的优势是动态灵活，然而太灵活了，大型工程难以保证质量，这也是 Chrome 发布了内置 DartVM 的版本，尝试用 Dart 取代 JavaScript 的原因之一。虽然这个超前的尝试失败了，但也说明Google并不看好 Javascript，至少 Dart 比它先进。Google内部很多项目(如内部广告系统)都采用 Dart 来生成 Web前端了。 Flutter 携 Dart 之先进性，开启了统一 App/PC/Web 的征途。试问谁还会在乎 Javascript 的前景呢？多端大统一是大趋势，Javascript 程序员应该积极拥抱这种变化。
        - 如果只能推荐一本JavaScript的书，推荐《The Modern JavaScript Tutorial》，中文名《现代 JavaScript 教程》。
        - 这个教程是 [React 官方文档中与 MDN 并列推荐](https://link.zhihu.com/?target=https%3A//zh-hans.reactjs.org/docs/getting-started.html%23javascript-resources)的 JavaScript __学习__教程。
            - **这个教程主要分为三个部分：** **入门：**主要为 JavaScript 语言方面的内容，包括__数据__类型，循环，对象，闭包，Class，原型，继承，Promise，ES Module 等基础__知识__。**提升：**包括 BOM 和 BOM 的相关内容。**进阶：**包括__网络__请求，Web Components，正则，动画，浏览器缓存等相关内容。
        - 这个过程中，你会发现网页特效如banner焦点图切换，点击下拉再点击又关闭等效果以及字符串的检测等功能都可以在网上搜到很多现成的代码可以用，于是你就会觉的不亦乐乎，前端可以如此简单。
- [[可视化]]library
    - [[d3.js]]
- 只需要一个浏览器就可以学习javascript，环境配置真是简单。
-  Roam JS Extensions#[[Roam Research]]
  via[Roam JS Extensions](https://roam.davidvargas.me/)
  [[20201228]] 下午5:36
- 开发框架
    - [[vue]]
    - [[react]]
    - [[angular]]
- 重要的库
    - [[jQuery ]]
    - [[bootstrap]]
- 基于JavaScript的控制面板在快速授权访问数据科学结果方面是完美的，因为它们只要求用户有一个Web浏览器。替代方案也有，比如Qlik（第5章）。
  ·[[Crossfilter]]是一个[[MapReduce]]库，是众多JavaScript MapReduce库之一，但是它的稳定性得到了证明，并且被一家从事金融交易的公司Square所开发和使用。采用MapReduce是有效的，甚至在单一的节点上和一个浏览器上，它能够提高计算速度。
  ·dc.js是创建于[[d3.js]]和Crossfilter之上的图表库，支持浏览器控制面板的快速构建Via[Python数据科学导论 - 得到APP](https://www.dedao.cn/reader?id=V5R16yPmaYOMqGRAv82jkX4KDe175w7VJa3rbx6pNgznl9VZPLJQyEBodb89mqoO)[[20210104]] 上午10:05
- 声明变量
    - 2.变量的命名规范😀😀1）变量名只能由字母、数字、下画线、$组成，且开头不能是数字。😀😀2）变量区分大小写，大写字母与小写字母为不同变量。😀😀3）变量名命名要符合两大法则之一。😀😀
      ①小驼峰法则：变量首字母为小写，之后每个单词首字母大写（常用）。😀😀
      ②匈牙利命名法：变量所有字母都小写，单词之间用下画线分隔。😀😀例如：😀😀helloJavaScript  正确写法（小驼峰法则）√hello_java_script  正确写法（匈牙利命名法）√hellojavascript  错误写法×Via[Web前端学习笔记：HTML5+CSS3+JavaScript - 得到APP](https://www.dedao.cn/reader?id=L5BbmPyQPrjybo2eO1GvAmNJnlYxV0Rq59w8XDBK9qZpgkRELd75z4Ma6oDRrqjY) [[20210114]] 上午9:09
- 变量的类型
    - 在JavaScript中，基本数据类型有很多，后面章节要讲解的数组、正则都算是数据类型，而ES6（JavaScript的最新标准，后续讲解）也新增了很多种数据类型。但是，一旦提到基本数据类型，JavaScript中只有6种。
        - 1.Undefined：未定义😀😀在JavaScript中，使用var声明变量，但没有进行初始化赋值时，结果为Undefined。如果变量没有声明直接使用，则会报错，不属于Undefined。Via[Web前端学习笔记：HTML5+CSS3+JavaScript - 得到APP](https://www.dedao.cn/reader?id=L5BbmPyQPrjybo2eO1GvAmNJnlYxV0Rq59w8XDBK9qZpgkRELd75z4Ma6oDRrqjY) [[20210114]] 上午9:11
        - 2.NULL：空引用。NULL在JavaScript中是一种特殊的数据类型，表示一种空的引用，也就是这个变量中什么都没有。同时，NULL作为关键字不区分大小写，形如“NULL”“Null”“null”均为合法数据类型。var a=null；
        - 3.Boolean：布尔类型
          Boolean值是一种非常常用的数据类型，表示真或者假，可选值只有两个：true或false。代码示例如下：
          var a=true；  //a直接被赋值为true
          var b=1＞2；  //b通过计算，被赋值为false
          console.log（a）；
          console.log（b）；Via[Web前端学习笔记：HTML5+CSS3+JavaScript - 得到APP](https://www.dedao.cn/reader?id=L5BbmPyQPrjybo2eO1GvAmNJnlYxV0Rq59w8XDBK9qZpgkRELd75z4Ma6oDRrqjY) [[20210114]] 上午9:12
        - 4.Number：数值类型
          在JavaScript中，没有区分整数类型和小数类型，而是统一用数值类型代替。例如，整数类型和小数类型都输入Number类型：
          var a=11；  //a整数类型
          var b=11.2；  //b小数类Via[Web前端学习笔记：HTML5+CSS3+JavaScript - 得到APP](https://www.dedao.cn/reader?id=L5BbmPyQPrjybo2eO1GvAmNJnlYxV0Rq59w8XDBK9qZpgkRELd75z4Ma6oDRrqjY) [[20210114]] 上午9:13
        - 5.String：字符串类型
          使用双引号（""）或单引号（''）包裹的内容，被称为字符串。两种字符串没有任何区别，且可以互相包含。代码示例如下：
          var a="我在'杰瑞教育'上课"；  //使用双引号声明字符串，双引号中可以包裹单引号var b='我在"杰瑞教育"上课'；  //使用单引号声明字符串，单引号中可以包裹双引号console.log（a）；
          console.log（b）
        - 6.Object：对象类型
          Object是一种对象类型。在JavaScript中有一句话“万物皆对象”，包括函数、数组、自定义对象等都属于对象类型，本书将在后续章节进行详细讲解。
- [[DOM]]
- 原型与原型链😀😀原型与原型链是JavaScript中最重要的一个环节。可以说理解了原型与原型链的思想，才能够算是真正学会了JavaScript。首先，需要理解什么是__proto__和prototype。而一个对象的__proto__的最终指向，就是这个对象的原型链。Via[Web前端学习笔记：HTML5+CSS3+JavaScript - 得到APP](https://www.dedao.cn/reader?id=L5BbmPyQPrjybo2eO1GvAmNJnlYxV0Rq59w8XDBK9qZpgkRELd75z4Ma6oDRrqjY) [[20210114]] 上午10:32
- #[[参考资料]]
    - [JavaScript基础语法-dom-bom-js-es6新语法-jQuery-数据可视化echarts黑马pink老师前端入门基础视频教程(500多集)持续_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=456) [[20210909]] 上午11:53
    - [2019全新javaScript进阶面向对象ES6_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1Kt411w7MP?p=10) [[20210909]] 上午11:53
    - JavaScriptVia[JavaScript | MDN](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript)[[20210104]] 下午9:22 @评论:感觉这个教程不错
    - {{[[video]]: https://youtu.be/EfAl9bwzVZk}}
    - Want to learn JavaScript in 2021 ?
      Here's a Roadmap for youVia[(3) Nirbhay Vashisht 在 Twitter: "Want to learn JavaScript in 2021 ? Here's a Roadmap for you🧵👇" / Twitter](https://twitter.com/nirbhayvashisht/status/1346332985369378817)[[20210105]] 下午2:35
    - javascript
        - [jQuery之家-自由分享jQuery、html5、css3的插件库](http://www.htmleaf.com/)
        - [jQuery插件库-收集最全最新最好的jQuery插件](https://www.jq22.com/)
        - [Bootstrap中文网](https://www.bootcss.com/)
        - [Bootstrap v3 中文文档 · Bootstrap 是最受欢迎的 HTML、CSS 和 JavaScript 框架，用于开发响应式布局、移动设备优先的 WEB 项目。 | Bootstrap 中文网](https://v3.bootcss.com/)
        - [Examples - Apache ECharts](https://echarts.apache.org/examples/zh/index.html#chart-type-line)
            - [现代 JavaScript 教程](https://zh.javascript.info/)
                - [Importing data from theBrain into DT - DEVONthink - DEVONtechnologies Community](https://discourse.devontechnologies.com/t/importing-data-from-thebrain-into-dt/57007/31) #[[软件联动]]
                - [Export TheBrain to Obsidian, a small script - Share & showcase - Obsidian Forum](https://forum.obsidian.md/t/export-thebrain-to-obsidian-a-small-script/6641/3) #[[软件联动]]
                - [JavaScript 库 | 菜鸟教程](https://www.runoob.com/js/js-libraries.html)
                - [jQuery 教程 | 菜鸟教程](https://www.runoob.com/jquery/jquery-tutorial.html)
