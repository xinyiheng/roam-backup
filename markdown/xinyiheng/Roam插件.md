- # chrome插件商店中的插件
    - [[roam portal]]可以展示概念之间的立体图，非常棒，我设置了
#[[快捷方式]]ctrl+p
    - [[Roam Highlighter]]
    - [[roam toolkit]]很早就安装了，但是很少使用，最近知道了它可以把卡片以思维导图的方式展示出来，感觉很惊艳，可以使用。我设置了调出这个插件的#[[快捷方式]]ctrl+i
        - ```javascript
```
- # [[roam extentions]]
    - 基本上都是以[[roam/js]]为开头的
        - ExtensionsVia[RoamJS Extensions](https://roamjs.com/extensions) [[20220117]] 上午10:21 @评论:这是最全的一个寻找roam插件的地方。它还推出了一个叫做、的插件专门管理下载的插件，可以说层层嵌套了。
        - unlink-finder
            - {{[[roam/js]]}}
                - ```javascript
var s = document.createElement('script');
	s.type = "text/javascript";
  	s.src =  "https://tylerwince.github.io/roam-plugins/unlink-finder/unlink-finder.js";
  	s.async = true;
document.body.appendChild(s);```
                - ## Example CSS
                    - 
.exact-word-match.unlink-finder,
.unlink-finder-legend.exact-word-match.unlink-finder {
  background-color: darkgreen;
  border-radius: 2px;
  text-decoration: none !important;
}
.fuzzy-word-match.unlink-finder,
.unlink-finder-legend.fuzzy-word-match.unlink-finder {
  background-color:  darkorange !important;
  text-decoration: none !important;
}
.partial-word-match.unlink-finder,
.unlink-finder-legend.partial-word-match.unlink-finder {
  background-color:  brown !important;
  text-decoration: none !important;
}
.redundant-word-match.unlink-finder,
.unlink-finder-legend.redundant-word-match.unlink-finder {
  background-color: slategrey !important;
  text-decoration: none !important;
}
- # 独立开发者插件
    - 基于[[roam/js]]开发的
    - 卡片写作@评论:吕立青开发的js，我喜欢的主题。
        - {{[[roam/js]]}}
            - ```javascript
window.URLScriptServer = `https://styled-roam.vercel.app/`
window.styledRoamDisabledFeatures = [
  // 'CardListMode',
  // 'CardFlowMode',
  // 'TreeTableMode',
  // 'DocumentMode',
  // 'CalendarMode',
  // 'DownloadMode',
  // 'FocusMode',
]

var existing = document.getElementById('styled-roam')
if (!existing) {
  var extension = document.createElement('script')
  extension.src = window.URLScriptServer + 'js/index.js'
  extension.id = 'styled-roam'
  extension.async = true
  extension.type = 'text/javascript'
  document.getElementsByTagName('head')[0].appendChild(extension)
}
```
    - 实验@评论:我自己学习js的时候尝试在roam中看看效果，目前并没有维护
    - masonry-vanilla @评论:数字花园
        - {{[[roam/js]]}}
            - ```javascript
:root {
    --main-left-bg: white;
    --right-sidebar-bg: rgb(247 248 249);
    --right-sidebar-drag-bg: #337ac6;
    --masonry-bg: white;
    --masonry-scrollbar-bg: lightgrey;
    --masonry-resizer-color: lightgrey;
    --masonry-startWidth: 550px; /* DEFAULT: 550px; Use "unset" to prevent loading in grid like format */
    --masonry-minWidth: 440px;
    --masonry-maxWidth: 1200px;
    --masonry-startHeight: 234px; /* DEFAULT: 243px; Use "unset" to prevent loading in grid like format */
    --masonry-minHeight: 200px;
    --masonry-border: 1px solid lightgrey;
    --closed-bullet-color: 4px solid #CED9E0;
    --code-color: crimson;
    --block-widths: 800px; /* Roam native: 800px; Murf's favorite: 1500px; Full screen: 3400px; */
}```
        - {{[[roam/js]]}}
            - ```javascript
var tfps = document.createElement("script");
tfps.type = "text/javascript";
tfps.src = "https://gitmurf.github.io/masonry-vanilla/JS/toggleFullPageScroll.js";
document.getElementsByTagName("head")[0].appendChild(tfps);```
        - {{[[roam/js]]}}
            - ```javascript
var mms = document.createElement("script");
mms.type = "text/javascript";
mms.src = "https://gitmurf.github.io/masonry-vanilla/JS/matuschakModeSizer.js";
document.getElementsByTagName("head")[0].appendChild(mms);```
    - excalidraw
        - [[roam/excalidraw]]
        - 来源：https://roamresearch.com/#/app/Zsolt-Blog/page/6uptQqZEV  
        - @评论:还有一个版本，我用着无效。[Roam-Excalidraw Plugin MVP Release](https://www.zsolt.blog/2021/03/roam-excalidraw-plugin-mvp-release.html) 之前画的图都失效了。
    - Telegroam
        - {{roam/js}}
            - ```javascript
var existing = document.getElementById("telegroam");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://telegroam.vercel.app/main.js";
  extension.id = "telegroam";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}```
- # Roam Depot
    - 如何查看和管理从roam depot安装的插件？在设置中进行
![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FWIxL8t52A0.png?alt=media&token=66f4f85d-763c-43fc-8e58-2235e3d87a70)
    - [[WorkBench]] ，🗒@评论:就是原来的roam42，还算是一个最重要的插件，有很多功能。
    - RANDOM BLOCK，会在左侧边栏生成一个图标，点击就会获得一个随机block，很不错的小玩具。
    - Memo 🗒@评论:这是一款[[间隔记忆]]工具，以前使用一款叫做js/sr的插件，但这款官方推出的界面更好看，是卡片的样式
    - {{[[TODO]]}} [[SmartBlock]] 🗒@评论:虽说很重要，但我并不太会用，以前的旧版本也很少使用
    - [[Universal Quick Capture]] 🗒@评论: 和[[Todolist]]联动，通过todolist这款软件向roam research添加笔记。这是今天最重要的发现。
    - {{[[TODO]]}} Query Builder，以前也有一款，新的这款功能更全，但看起来很复杂，我还不会用。
    - [[Toggle Track]]
    - Reference Path，可以展示当前block的路径，以前也有一款类似的，不过我用了卡片视图以后就失效了。这款好像有效。
    - Roam Studio，一款设置roam research外观的插件，我安装之后感觉使用体验好了很多。我之前自己调整了很多css，一些细节看起来不太好，用上这款以后感觉耳目一新。我开始更多地在笔记中使用markdown标题了，这样可以让笔记看起来更整齐。
    - Elapsed Time Calculator，一款在roam中辅助进行时间管理的工具，属于锦上添花的类型
    - {{[[TODO]]}} [[Twitter]] 🗒@评论:同名插件可以在roam中直接发送twitter信息，也可以把twitter动态导入到roam中。
    - Show Favicon，可以让roam中的网址前面带上一个该网址的小图标，安装之后网址美观了不少。
    - Export Fomatter，导出roam 中的block的时候可以设置格式，去除一些特殊格式，让导出的文件看起来更好看。注意，不能导出整个page，只能用于导出某个节点。用右键中的plugins来选择。
![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FD1Dw3Lw-R0.png?alt=media&token=75151243-7600-4992-898e-875942b35fb0)
有一个类似的Workbench Format Converter，ctr+m换出，可以支持导出整个page。
    - Image Generator，也是右键plugins中选择，可以根据一段英语来自动生成一幅[[人工智能画画]]产生的图片
    - Toggle Text Uppercase/Lowercase，也是右键plugins中选择，可以把一行的英语全变成大写或者小写。但是不能只首字母大写。
    - roam/comments，很早就安装了，但没有用过。今天才发现用法是按住cmd键，右侧会出现一个加号，点击加号就可以添加评论了。我以前总是在行内用特殊符号加评论，比如🗒@评论: 我就是这样评论的。
    - [[roam/comments] 🗒@评论:
        - [[December 23rd, 2022]]
            - [[Anonymous]]
                - roam/comments，很早就安装了，但没有用过。今天才发现用法是按住cmd键，右侧会出现一个加号，点击加号就可以添加评论了。我以前总是在行内用特殊符号加评论，比如🗒@评论: 我就是这样评论的。
                    - 这是用这种插件方式的评论
    - Sticky Headings，开启后，roam page中的标题在向下滑动页面的时候会冻结在页面可视范围的上方。这样看内容的时候总是可以看到标题。
    - Table of Contents，用cmd+p打开控制面板，然后找到toc，就可以为当前页面生成一个目录。
    - [todo-teleport](https://github.com/mlava/todo-teleport)，可以把没有完成的todo转移到别的日期。🗒@评论:用法可以参见链接。感觉可以完成[[子弹笔记]]的要求。 首先要把多个todo任务都选中，选中的方法是cmd+m，按下之后roam会自动隐藏起来，没事，再打开就会发现每个block的右侧都有一个小方框，点击方框就可以选中。在控制面板中选择todo-teleport就可以把未完成的任务转移到指定日期了。
        - {{[[DONE]]}} 实验1
        - {{[[TODO]]}} 实验2
        - {{[[TODO]]}} 实验3
