- bp3-popover-wrapperUsing Roam/CSS to display a list as grid or in rows
via[Using Roam/CSS to display a list as grid or in rows](https://www.loom.com/share/06b03473bcda4728b5bef40929e5012f)
[[20201230]] 上午10:14官方推出的一些css样式，用视频的形式展示出来的，比较直观
- Element Class Detail 发现没有关联的概念
    - Class: `exact-word-match`
        - Criteria
            - Case-Sensitive Match
            - Match is a complete word, not part of a word
            - Word is not already linked in a parent block
        - Example
            - You have a page called `link` and it matches a word `link`
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Ftylerwince%2Fim9emHjoe1.png?alt=media&token=278bd9e0-57fe-4bec-896e-17cb9cfefb4a)
        - Default Style
            - These are underlined in the same color as the text.
                - In the example, the color is black.
    - Class: `fuzzy-word-match`
        - Criteria
            - Case-insensitive match
        - Example
            - You have a page called `link` and it matches a word `LINK`
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Ftylerwince%2F0Wf5trJvpB.png?alt=media&token=4eec4fdb-2f0b-45f1-b159-d6f886320376)
        - Default Style
            - These are underlined in css gray
    - Class: `partial-word-match`
        - Criteria
            - Match found but it is a substring of another word
        - Example
            - You have a page called `link` that matches in a word `linked`
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Ftylerwince%2FNsFoGrgFKM.png?alt=media&token=270efc93-0749-47c4-aa53-4b7b4beabaff)
        - Default Style
            - These are underlined in css lightgray
    - Class: `redundant-word-match`
        - Criteria
            - Any match where the matched page is linked in a parent block. Creating this link again would be redundant.
        - Example
            - You have a page called `link` and the match is nested under a block already referencing that page.
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Ftylerwince%2FxNGU82eQvP.png?alt=media&token=28ab0832-404b-4b2f-b3ab-0a0bc9eaaf4b)
        - Default Style
            - These have a transparent underline, essentially no indicator. If you want them to show, you can change the `text-decoration-color` to whatever you prefer in roam/css
    - match
        - ```css
.exact-word-match.unlink-finder,
.unlink-finder-legend.exact-word-match.unlink-finder {
  background-color: lightblue;
  border-radius: 2px;
  text-decoration: none !important;
}
.fuzzy-word-match.unlink-finder,
.unlink-finder-legend.fuzzy-word-match.unlink-finder {
  background-color:  pink!important;
  text-decoration: none !important;
}
.partial-word-match.unlink-finder,
.unlink-finder-legend.partial-word-match.unlink-finder {
  background-color:  lightgreen !important;
  text-decoration: none !important;
}
.redundant-word-match.unlink-finder,
.unlink-finder-legend.redundant-word-match.unlink-finder {
  background-color: lightyellow !important;
  text-decoration: none !important;
}```
        - 
        - .unlink-finder-legend.exact-word-match.unlink-finder {
            - background-color: darkgreen;
            - border-radius: 2px;
            - text-decoration: none !important;
        - }
        - .fuzzy-word-match.unlink-finder,
        - .unlink-finder-legend.fuzzy-word-match.unlink-finder {
            - background-color:  darkorange !important;
            - text-decoration: none !important;
        - }
        - .partial-word-match.unlink-finder,
        - .unlink-finder-legend.partial-word-match.unlink-finder {
            - background-color:  brown !important;
            - text-decoration: none !important;
        - }
- 思维导图模式
    - ```css
/* Created by: @Calhistorian (Mark Robertson) */

.blockmap {
  display: flex;
  align-items: left;
  flex-direction: row;
  align-items: baseline; /* allows Azlan's path finder to not go "up" */
  justify-content: baseline;

}
 
.blockmap div {
 border:none;

} 

.blockmap .rm-block__self  {
  width: 400px; /* Adjust this value for block width */
  padding: 10px 10px;
}

.blockmap .rm-block__children {
  margin-top: 5px;
  margin-bottom: 5px;
}

/* Horizontal Scrolling */
.roam-body-main > div  {
  overflow-x: scroll !important;
}```
- 美化youtube时间戳的按钮分享一个Andy Mode的CSS和几个js插件https://github.com/GitMurf/masonry-vanilla#masonry-vanilla
    - ```css
.timestamp-control{
  background-color: rgba(108,109,36,0.1); 
  color: rgb(251,106,13);
  margin-right: 8px;
  margin-top: 0px;
  margin-left: 0px;
  margin-bottom: 5px;

  border-radius: 50% !important;
  border-style: inset;  
  border-color: #FF3200;
  font-size: 0.9em;
}
.timestamp-control:hover {
  background-color: rgba(108,109,36,0.25); 
  border-style: outset;  
  color: #FFFFFF;
}```
- kanban
    - ```css

.kanban-board {
  background-color: #FFDB3A;
  max-height: 600px; 
  overflow-x: auto;
  overflow-y: auto;
}

.kanban-column {
  background-color: rgba(248,227,187,0.98);
}

.kanban-card {
  box-shadow: 0 1px 4px 0 rgba(21, 27, 38, 0.08);
  border-radius: 4px;
  box-shadow: 0 1px 4px 0 rgba(21, 27, 38, 0.08);
}

roam-block-container rm-block rm-block--mine rm-block--open rm-not-focused block-bullet-viewroam-block-container rm-block rm-block--mine rm-block--open rm-not-focused block-bullet-view.kanban-card:hover {
  box-shadow: 0 3px 5px 0 rgba(0, 0, 0, 0.1);
  transform: translateY(-1px);
}

.kanban-title {
  text-align: left;
  margin: 0px 8px;
  font-weight: 700px;
  border-bottom: none;
}```
- pdf优化
    - ```css
:root{
  --col1: rgba(255, 243, 174, .8);
  --col2: rgba(255, 132, 132, .8);
  --col3: rgba(155, 253, 130, .8);
  --col4: rgba(130, 169, 255, .8);
  --col5: rgba(220, 131, 255, .7);
  --col6: rgba(172,172,172, .7);
}

[data-tag^="h:"] {
  display:none !important;  
}

[data-tag^="h:"] + .rm-highlight, 
[data-tag^="h:"] + span > .rm-page-ref--link {
  color: rgb(0,0,0) !important;
  /*border-radius: 5px;
  padding-left: 5px;
  padding-right: 5px;
  font-weight: bold;*/
}

[data-tag^="h:yellow"] + .rm-highlight,
[data-tag^="h:yellow"] + span > .rm-page-ref--link {
	background-color: var(--col1) !important;
}
[data-tag^="h:yellow"] + .rm-italics, 
[data-tag^="h:yellow"] + .rm-bold 
{color: var(--col1);}

[data-tag^="h:red"] + .rm-highlight,
[data-tag^="h:red"] + span > .rm-page-ref--link {
	background-color: var(--col2) !important;
}
[data-tag^="h:red"] + .rm-italics, 
[data-tag^="h:red"] + .rm-bold 
{color: var(--col2); }


[data-tag^="h:green"] + .rm-highlight,
[data-tag^="h:green"] + span > .rm-page-ref--link {
	background-color: var(--col3) !important;
}
[data-tag^="h:green"] + .rm-italics, 
[data-tag^="h:green"] + .rm-bold 
{color: var(--col3); }

[data-tag^="h:blue"] + .rm-highlight,
[data-tag^="h:blue"] + span > .rm-page-ref--link {
	background-color: var(--col4) !important;
}
[data-tag^="h:blue"] + .rm-italics, 
[data-tag^="h:blue"] + .rm-bold 
{color: var(--col4); }

[data-tag^="h:purple"] + .rm-highlight,
[data-tag^="h:purple"] + span > .rm-page-ref--link {
	background-color: var(--col5) !important;
}
[data-tag^="h:purple"] + .rm-italics, 
[data-tag^="h:purple"] + .rm-bold 
{color: var(--col5); }

[data-tag^="h:grey"] + .rm-highlight,
[data-tag^="h:grey"] + span > .rm-page-ref--link {
	background-color: var(--col6) !important;
}
[data-tag^="h:grey"] + .rm-italics, 
[data-tag^="h:grey"] + .rm-bold 
{color: var(--col6); }

/*All btns*/
.btn{padding: 0px !important;  border: 3px !important;}

/*All main highlight btns*/
.btn-pdf-activated{
  border-radius: 14px !important;
  font-size: 12px !important;
  font-weight: bold;
  min-width: 18px !important;
  min-height: 18px !important;
  margin-top: 3px !important;
}

.btn-main-annotation{
  background-color : rgb(221,220,220) !important;
  color: rgb(0,0,0); 
  margin-top: 0px !important;
}

/*All reference to highlight buttons*/
.btn-rep-text{
}
.btn-rep-alias{
}
.btn-ref-annotation{
  background-image: linear-gradient(rgb(249,249,49), rgb(246,246,170), rgb(210,210,9));
  color: rgb(6,6,6);
}

/* Hide PDF Breadcrumb */
.parent-path-wrapper > div > span > div > div {
  display: none;
}
```
- [[Tag Styles]]
    - {{[[roam/css]]}}
        - ```css

/* Custom data tags */
span.rm-page-ref[data-tag="写作"] {
    background: #81D5ED !important;
    color: white !important;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="参考资料"] {
    background: #9769FF !important;
    color: white !important;
    padding: 3px 7px;
    font-weight: 500;
    line-height: 2em;
}

span.rm-page-ref[data-tag="读书笔记"] {
    background: #FF9800EA !important;
    color: white !important;
    padding: 3px 7px;
    font-weight: 500;
    line-height: 2em;
}

span.rm-page-ref[data-tag="Evergreens"] {
    background: #0DBAC6 !important;
    color: #EBDAA8 !important;
    padding: 3px 8px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Seedling"] {
    color: #0dbac6 !important;
    padding: 3px 3px;
    font-weight: 600;
    line-height: 1.4em;
}

span.rm-page-ref[data-tag="Idea Bank"] {
    color: #FCB815 !important;
    padding: 3px 4px;
    font-weight: 700;
    line-height: 1.4em;
}

span.rm-page-ref[data-tag="洞见"]:before {
    content: '✦ '
}

span.rm-page-ref[data-tag="Illustrated Notes"] {
    color: #7172FC;
    padding: 3px 4px;
    font-weight: 700;
    line-height: 1.4em;
}

span.rm-page-ref[data-tag="Garden Notes"] {
    color: #9DBC13;
    padding: 3px 4px;
    font-weight: 700;
    line-height: 1.4em;
}

span.rm-page-ref[data-tag="问题"] {
    color: #030B0F;
    background: #F44336 !important;
    padding: 3px 4px;
    line-height: 1.4em;
    font-weight: 700;
}

span.rm-page-ref[data-tag="软件联动"] {
    background: #ADCB2A;
    color: #fff;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}


span.rm-page-ref[data-tag="Livestream"] {
    color: #8C41A6;
    padding: 3px 4px;
    line-height: 1.4em;
    font-weight: 700;
}

span.rm-page-ref[data-tag="Talk"] {
    background: #7172FC;
    color: #fff;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Waiting"] {
    background: #F9C866;
    color: #fff;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Researching"] {
    background: #FF9D66 !important;
    color: #fff;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Synthesising"] {
    background: #FC766F !important;
    color: #fff !important;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}


span.rm-page-ref[data-tag="Alive"] {
    background: #EE5F85 !important;
    color: #fff !important;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}```
- ^^tag^^
    - ```css
span.rm-page-ref[data-tag] {    
  background-color: #D2F89C;    
  color: black;    
  padding: 3px 7px;    
  line-height: 1em;    
  border-right: solid 1px;    
  border-bottom: solid 1px;    
  border-radius: 3px;    
  font-weight:500;
}```
- ^^秘密花园^^
    - ```css

:root {
    --main-left-bg: #BECEFC;
    --right-sidebar-bg: #9FD8D3(247 248 249);
    --right-sidebar-drag-bg: #337ac6;
    --masonry-bg: #F1F7FA;
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
}
#right-sidebar, div.roam-app>div.flex-h-box {
    background-color: var(--right-sidebar-bg);
}
/*修改url链接的文字颜色*/
a {
  color:#9708AE !important;
}
/*修改链接颜色以及隐藏双方括号*/
.rm-page-ref {
  font-weight:bold;
  color:#009688;
}
.rm-page-ref__brackets{
  display:none;
}
/*修改最顶端栏目的背景*/
.rm-topbar {
  background-size:100%;
  background-image:url(https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FZE0d6w50_4.jpeg?alt=media&token=f67f5222-4df2-4c1e-aa9c-37ebcb8b0068);
}
/*修改unlinked references字体颜色*/
strong {
  	color:rgb(217,36,36)!important;
}
/*修改看板的样式*/
.kanban-board {
   background-color: skyblue;
   background-image:url("https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FFJiT_TGxLh.png?alt=media&token=ee76eead-1e43-47d6-9c02-6508e86f909f");
   background-size:100% 100%;
}
.kanban-column {
  background-color: rgba(210,227,233,0.65);
}
/*修改大卡片的样式*/
.card-mode .rm-block__children.rm-level-0>.roam-block-container, .card-mode [style="margin-left: -20px;"]>.roam-block-container, .presentation-card-mode .rm-block__children.rm-level-0>.roam-block-container, .presentation-card-mode [style="margin-left: -20px;"]>.roam-block-container {
    box-shadow: 8px 8px 16px 0 rgb(0 0 0 / 6%);
    border-radius: 8px;
    background: #f2f4f8;
    padding: 10px 16px 10px 0;
    margin: 16px;
    min-height: 200px;
    max-width: 600px;
    min-width: 400px;
}
/*修改高亮文字背景色*/
.rm-highlight {
  background-color: rgb(31,180,32);
}
/*修改编辑中的文字字体*/
textarea {
    font-family: 简宋;
}
/*修改选中后的文字颜色*/
::selection {
    background: #DC6767;
}
/*修改左侧边栏文字颜色*/
.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .starred-pages-wrapper .starred-pages .page {
    text-decoration: none;
    cursor: pointer;
    font-size: 16px;
    padding: 4px 0px 4px 4px;
    color: #439AF6;
}
/*修改笔记主题的字体*/
div {
    font-family:简宋;
}
/*设置笔记主题的背景色和背景图片*/


div.roam-app>div.flex-h-box>div.roam-main>div.roam-body-main {
    
  	background-image:url("https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FZE0d6w50_4.jpeg?alt=media&token=f67f5222-4df2-4c1e-aa9c-37ebcb8b0068");
    background-size:100% 100% ;
}
/*设置左侧边栏背景色*/
.roam-body .roam-app .roam-sidebar-container {
    background-color: #293840;
}

#roam-right-sidebar-content {
    overflow: auto !important;
}
#247EC2#1480D3#1476D3##C6C067
.sidebar-content {
    overflow: unset;
    display: flex;
    background-color: rgb(202,114,114);
    flex-direction: column;
    flex-wrap: wrap;
    height: 99%;
    align-content: flex-start;
}
/*设置卡片模式下卡片的颜色和背景阴影的颜色，我花了很多时间才学会*/
.flow-mode .roam-article>div:first-child .rm-block-main.rm-block__self {
    width: 370px;
    height: 200px;
    margin: 20px;
    box-shadow: 8px 8px 16px 0 rgb(29 0 0 / 76%);
    border-radius: 8px;
    background: hsl(132,29%,97%);
    background-size: 100% 100%;
    background-position: 0px 2px;
    background-image: url("");
    padding: 20px 16px 16px 0;
}
.sidebar-content>div:not(.rm-dnd-separator) {
    margin-bottom: 10px !important;
    display: flex;
    background-color: var(--masonry-bg);
    max-height: 100%;
    margin-left: 15px;
    align-self: flex-start;
    /* So pages can be diff widths in a single column */
    border-radius: 12px;
    border: var(--masonry-border);
}

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator) {
    border-bottom: unset !important;
    height: 100%;
    padding-top: 10px;
    padding-bottom: 10px;
}

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:first-child {
    height: 40px;
    min-width: calc(var(--masonry-minWidth) + 40px);
    align-items: center !important;
}

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2) {
    height: calc(100% - 40px);
}

/*NOTE: .rm-sidebar-outline and .rm-reference-main are at same level and so need to be addressed with div > div... as opposed to direct .classnames */

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(1) {
    resize: both;
    overflow-y: auto;
    width: var(--masonry-startWidth);
    min-width: var(--masonry-minWidth);
    max-width: var(--masonry-maxWidth);
    height: var(--masonry-startHeight);
    min-height: var(--masonry-minHeight);
    max-height: 100%;
    margin-right: 8px;
}

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(1)>div:nth-child(2) {
    padding-bottom: 40px;
    margin-left: -8px !important;
}

.sidebar-content .rm-reference-main>div {
    margin-left: 0px !important;
    margin-right: 5px !important;
    padding-bottom: 40px;
}

/* SCROLLBAR */

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(1)::-webkit-scrollbar {
    width: unset;
}

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(1)::-webkit-scrollbar:hover {
    background-color: var(--masonry-bg);
}

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(1)::-webkit-resizer {
    border-style: solid;
    border-color: transparent var(--masonry-resizer-color) var(--masonry-resizer-color) transparent;
    background-color: var(--masonry-bg);
    border-width: 3px;
}

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(1)::-webkit-scrollbar-button, .sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(1)::-webkit-scrollbar-thumb, .sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(1)::-webkit-scrollbar-track, .sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(1)::-webkit-scrollbar-track-piece, .sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(1)::-webkit-scrollbar-corner {
    display: none;
}

/*Make the scrollbar smaller but keep the resize button the same*/

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(1):hover::-webkit-scrollbar-thumb {
    display: block;
    border-radius: 12px;
    background-color: var(--masonry-scrollbar-bg);
    border-style: solid;
    border-width: 6px;
    border-color: var(--masonry-bg);
}

/* Focus/zoom breadcrumb trail */

.roam-body-main .roam-article .zoom-path-view {
    margin-top: 10px;
}

/* Don't let images extend outside box */

.rm-inline-img__resize, .react-resizable {
    max-width: 100%;
}

/* When long page titles or block refs are in sidebar they need to be shrunk */

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div.flex-h-box.window-headers>div:nth-child(2) {
    max-width: calc(var(--masonry-minWidth) - 10px);
    max-height: 3em !important;
    overflow: hidden;
}

/* Drag n Drop */

.sidebar-content>div.rm-dnd-separator {
    left: 16px;
    top: -3px;
    width: calc(var(--masonry-minWidth));
}

.sidebar-content>div>div.rm-dnd-separator {
    right: 100%;
    top: 100%;
}

.sidebar-content .rm-dnd-separator .rm-dnd-drop-bar {
    top: 3px;
    left: 1px;
    background-color: var(--right-sidebar-drag-bg);
}



.sidebar-content .rm-dnd-separator {
    width: unset;
}

.rm-dnd-drop-area, .rm-dnd-drop-bar {
    min-width: calc(var(--masonry-minWidth) + 55px);
}

/* The new indent lines were showing on top of search bar */

/* Abhay said that him and jeff harris set to 8, but I needed to set to 4 to work */

.rm-multibar {
    z-index: 4;
}

/* Fix where block ref counter overflows and adds unnecessary horizontal scroll in masonry side pages */

div.rm-block-main {width: 99%;}

/* Kanban */

div[data-page-links*="kanban"] .dont-focus-block.rm-full-width {
    margin-right: unset;
}
div.roam-main .kanban-board .kanban-column {
    flex: 1 0 150px;
}
div#right-sidebar .kanban-board .kanban-column {
    flex: 1 0 75px;
}
```
    - ```css

/* Extend the main page wider to allow for blocks to be wider  */

div[style*="padding-right: calc((100% - 800px) / 2); padding-left: calc((100% - 800px) / 2);"], div[style*="padding-right: calc((100% - 568px) / 2); padding-left: calc((100% - 1032px) / 2);"] {
    /*
    Roam Default 800px
    padding-right: calc((100% - 800px) / 2) !important;
    padding-left: calc((100% - 800px) / 2) !important;

    FULL WIDTH
    padding-right: calc((100% - 3400px) / 2) !important;
    padding-left: calc((100% - 3400px) / 2) !important;
    */

    padding-right: calc((100% - var(--block-widths)) / 2) !important;
    padding-left: calc((100% - var(--block-widths)) / 2) !important;
}

/* Block text widths to extend block text wider for when you make the page wider with the CSS above  */

.roam-block-container {
    max-width: unset;
}

#right-sidebar .rm-block-children.rm-block__children.rm-level-0>div.roam-block-container, #right-sidebar div.zoom-path-view+div>div.roam-block-container {
    width: 98%;
}

.rm-block-text {
    max-width: unset;
}

#right-sidebar div.rm-zoom.zoom-path-view {
    width: 98%;
}

/* Allow images to resive full width */

.hoverparent[style^="width: 580px;"], .hoverparent[style^="width: 720px;"] {
    width: 100% !important;
    max-width: 1100px !important;
}

.rm-inline-img, .react-resizable[style^='width: 580px;'], .react-resizable[style^='width: 720px;'] {
    width: 100% !important;
}

/* Override image, iframe, pdf resize form abhay 1-30-21 */

div[style*="width: 580px;"], div[style*="width: 720px;"] {
    width: 100% !important;
    max-width: 1100px !important;
}

div[style*="height: 720px;"] {
    height: 85vh !important;
}

/* Search bar wide when typing in it */

/* These account for left sidebar being open and making sure search bar stays on top of it */
.roam-sidebar-container.noselect:hover {
    z-index: 1001;
}
.rm-topbar {
    z-index: 1000;
}

.rm-find-or-create-wrapper:focus-within {
    flex: 0 1 77% !important;
}

.bp3-overlay-open ul.bp3-menu .rm-menu-item li>span {
    max-height: 42px !important;
    word-break: break-word !important;
    overflow: hidden !important;
    display: inline-block !important;
}

.bp3-overlay-open ul.bp3-menu .rm-menu-item li {
    list-style-type: none !important;
    margin-left: -35px;
}

/* Buttons / Icons in menu area by search bar */

/* Filter button was kind of high and to the left */

.rm-topbar .bp3-button .bp3-icon.bp3-icon-filter {
    margin-top: 4px;
    margin-right: -18px;
}

/* Fixing the sidebar close button to show on very right of menu bar */

#right-sidebar .bp3-icon-menu-open {
    z-index: 1001;
    padding-top: 4px !important;
}
.rm-topbar {
    padding-right: 30px;
}

/* Add dashed line on hover of sidebar resizer line in middle of page */

.rm-resize-handle:hover {
    opacity: 0.4 !important;
    border-right: 2px dashed #1b1a23 !important;
    padding-left: 5px;
}

/* The "all collapse/expand" invisible line to very left of blocks */

.rm-level-0>.rm-multibar {
    opacity: 0.25;
}

/* Hide "Outline of: " in the sidebar except for block references because otherwise nowhere to grab for drag n drop. */

div.sidebar-content div.flex-h-box.window-headers>div:nth-child(2)>span:first-child:not([style^="margin-right: 6px"]) {
    display: none;
}

```
    - ```css

/* Extend the main page wider to allow for blocks to be wider  */

div[style*="padding-right: calc((100% - 800px) / 2); padding-left: calc((100% - 800px) / 2);"], div[style*="padding-right: calc((100% - 568px) / 2); padding-left: calc((100% - 1032px) / 2);"] {
    /*
    Roam Default 800px
    padding-right: calc((100% - 800px) / 2) !important;
    padding-left: calc((100% - 800px) / 2) !important;

    FULL WIDTH
    padding-right: calc((100% - 3400px) / 2) !important;
    padding-left: calc((100% - 3400px) / 2) !important;
    */

    padding-right: calc((100% - var(--block-widths)) / 2) !important;
    padding-left: calc((100% - var(--block-widths)) / 2) !important;
}

/* Block text widths to extend block text wider for when you make the page wider with the CSS above  */

.roam-block-container {
    max-width: unset;
}

#right-sidebar .rm-block-children.rm-block__children.rm-level-0>div.roam-block-container, #right-sidebar div.zoom-path-view+div>div.roam-block-container {
    width: 98%;
}

.rm-block-text {
    max-width: unset;
}

#right-sidebar div.rm-zoom.zoom-path-view {
    width: 98%;
}

/* Allow images to resive full width */

.hoverparent[style^="width: 580px;"], .hoverparent[style^="width: 720px;"] {
    width: 100% !important;
    max-width: 1100px !important;
}

.rm-inline-img, .react-resizable[style^='width: 580px;'], .react-resizable[style^='width: 720px;'] {
    width: 100% !important;
}

/* Override image, iframe, pdf resize form abhay 1-30-21 */

div[style*="width: 580px;"], div[style*="width: 720px;"] {
    width: 100% !important;
    max-width: 1100px !important;
}

div[style*="height: 720px;"] {
    height: 85vh !important;
}

/* Search bar wide when typing in it */

/* These account for left sidebar being open and making sure search bar stays on top of it */
.roam-sidebar-container.noselect:hover {
    z-index: 1001;
}
.rm-topbar {
    z-index: 1000;
}

.rm-find-or-create-wrapper:focus-within {
    flex: 0 1 77% !important;
}

.bp3-overlay-open ul.bp3-menu .rm-menu-item li>span {
    max-height: 42px !important;
    word-break: break-word !important;
    overflow: hidden !important;
    display: inline-block !important;
}

.bp3-overlay-open ul.bp3-menu .rm-menu-item li {
    list-style-type: none !important;
    margin-left: -35px;
}

/* Buttons / Icons in menu area by search bar */

/* Filter button was kind of high and to the left */

.rm-topbar .bp3-button .bp3-icon.bp3-icon-filter {
    margin-top: 4px;
    margin-right: -18px;
}

/* Fixing the sidebar close button to show on very right of menu bar */

#right-sidebar .bp3-icon-menu-open {
    z-index: 1001;
    padding-top: 4px !important;
}
.rm-topbar {
    padding-right: 30px;
}

/* Add dashed line on hover of sidebar resizer line in middle of page */

.rm-resize-handle:hover {
    opacity: 0.4 !important;
    border-right: 2px dashed #1b1a23 !important;
    padding-left: 5px;
}

/* The "all collapse/expand" invisible line to very left of blocks */

.rm-level-0>.rm-multibar {
    opacity: 0.25;
}

/* Hide "Outline of: " in the sidebar except for block references because otherwise nowhere to grab for drag n drop. */

div.sidebar-content div.flex-h-box.window-headers>div:nth-child(2)>span:first-child:not([style^="margin-right: 6px"]) {
    display: none;
}
```
