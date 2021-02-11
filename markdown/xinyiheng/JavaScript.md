- 好像roam之类的网页应用很多互动效果是通过javascript实现的。
- [[可视化]]library
    - [[d3.js]]
- 能够支持javascrpt的笔记工具应该可以实现更多的互动性。
- 只需要一个浏览器就可以学习javascript，环境配置真是简单。
-  Roam JS Extensions#[[roam research]]
via[Roam JS Extensions](https://roam.davidvargas.me/)
[[20201228]] 下午5:36
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
- 
- #[[参考资料]]
    - JavaScriptVia[JavaScript | MDN](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript)[[20210104]] 下午9:22 @评论:感觉这个教程不错
    - {{[[video]]: https://youtu.be/EfAl9bwzVZk}}
    - Want to learn JavaScript in 2021 ?
Here's a Roadmap for youVia[(3) Nirbhay Vashisht 在 Twitter: "Want to learn JavaScript in 2021 ? Here's a Roadmap for you🧵👇" / Twitter](https://twitter.com/nirbhayvashisht/status/1346332985369378817)[[20210105]] 下午2:35
