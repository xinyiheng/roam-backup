- ```css

/* 修改reference部分的背景颜色 */
.rm-reference-item {
    background-color: rgba(255,255,255,0)
}

/* 修改标签的字体并隐藏# */
.rm-page-ref--tag{font-family:简宋!important;
                  }


/* div.rm-level-0 > .roam-block-container.rm-block.rm-block--mine.rm-not-focused.block-bullet-view:not(.block-highlight-blue){
  margin:10px 20px 10px 10px;
}



/*修改引用的样式*/
.rm-bq {
  font-family:简宋!important;
}
/*修改referenc标题样式*/

/*修改referenc卡片样式*/
.flex-align-start {
    align-items: flex-start;
    background-color:#F2E9E96D; !important;
    margin: 10px;
    border-radius: 10px;
     box-shadow: 8px 8px 16px 0 rgb(0 0 0 / 22%), -8px -8px 16px 0 rgb(16 22 26 / 0%)!important;
}


/*修改右侧边栏背景样式*/
.sidebar-content {
  background:rgba(255,250,250,0)
}
div
{
  color: #010D14;
}
span[data-link-title$="2022"] .rm-page-ref-link-color::before{
    content: "🗓 ";
}
/* 解决block内部文字无法很接近右侧的问题 */
.rm-block-separator {
    flex: 0 0 0px;
    min-width: 0px;
}
/* card-flow-mode 文字溢出卡片修复 */
 .flow-mode .roam-block-container .rm-block-main {
    display: flex;
    align-items: flex-start;
    justify-content: flex-start;
    overflow:scroll;
}


/* card-flow-mode 全部铺开的设置 */
.flow-mode .roam-article>div:first-child .rm-block__children.rm-level-0>.roam-block-container {
  align-items: center;
  position: relative;   
  top:0;
}
#.roam-toolkit-spatial-mode{
  position:static;
} 
/* card-list-mode 文字重合的问题*/ 
.block-bullet-view {
    flex: 1 1 auto;
}
/* table-mode 全部铺开的设置 */
.table-mode .roam-article>div:first-child .rm-block__children.rm-level-0>.roam-block-container {
    width: calc(100vw - 30px)!important;
    border: 1px solid #bfccd6;
   align-items: center;
    border-bottom: none;
    background: #F2F4F800;
    position: relative;
    top: 50px;
    overflow-x: scroll;
    overflow-y: hidden;
    scrollbar-width: none;
    -ms-overflow-style: none;
}
/*修改笔记主题的字体*/
div {
    font-family: 简宋!important;
}

:root {
    --main-left-bg: rgb(210,157,157);
    --right-sidebar-bg: #EA9C9C(247 248 249);
    --right-sidebar-drag-bg: #337ac6;
    --masonry-bg: #F2FCF321;
    --masonry-scrollbar-bg: rgba(31,206,108,0.48);
    --masonry-resizer-color: rgb(10,188,23);
    --masonry-startWidth: 550px; /* DEFAULT: 550px; Use "unset" to prevent loading in grid like format */
    --masonry-minWidth: 440px;
    --masonry-maxWidth: 1200px;
    --masonry-startHeight: 234px; /* DEFAULT: 243px; Use "unset" to prevent loading in grid like format */
    --masonry-minHeight: 200px;
    --masonry-border: 1px solid rgb(200,198,198);
    --closed-bullet-color: 4px solid #CED9E0;
    --code-color: crimson;
    --block-widths: 1500px; /* Roam native: 800px; Murf's favorite: 1500px; Full screen: 3400px; */
}
.rm-bullet__inner {
  background-color:#1B1B19;
}
/*修改鼠标选中某个block时候的背景色*/
/*.roam-block-container:hover {
  background-color: #13EDEDA5;
}*/

修改url链接的文字颜色*/
a {
  color:#9708AEB5 !important;
}
/*修改链接颜色以及隐藏双方括号*/
.rm-page-ref {
  font-weight:bold;
  color:#DE1717;
}
.rm-page-ref__brackets{
  display:none;
}

/*修改unlinked references字体颜色*/
strong {
  	color:rgb(217,36,36)!important;
}
/*修改看板的样式*/
.kanban-board {
   background-color: rgba(135,206,235,0.35);
   background-image:url("");
   background-size:100% 100%;
}
.kanban-column {
  background-color: rgba(210,227,233,0.65);
}
/*修改大卡片的样式*/
.card-mode .rm-block__children.rm-level-0>.roam-block-container, .card-mode [style="margin-left: -20px;"]>.roam-block-container, .presentation-card-mode .rm-block__children.rm-level-0>.roam-block-container, .presentation-card-mode [style="margin-left: -20px;"]>.roam-block-container {
    box-shadow: 8px 8px 16px 0 rgb(0 0 0 / 22%), -8px -8px 16px 0 rgb(16 22 26 / 0%)!important;
    border-radius: 8px;
     background-color;white
    padding: 10px 16px 10px 0;
    margin: 16px;
    min-height: 200px;
    max-width: 600px;
    min-width: 400px;
}
/*修改高亮文字背景色*/
.rm-highlight {
  background-color: rgba(31,180,32,0.5);
}
/*修改编辑中的文字字体*/
textarea {
   font-family:简宋!important;
}
/*修改选中后的文字颜色*/
::selection {
    background: #4C52EE82;
}
::hover {
    background: #A94B4B77;
}
/*修改左侧边栏文字颜色*/
.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .starred-pages-wrapper .starred-pages .page {
    text-decoration: none;
    cursor: pointer;
    font-size: 14px;
    padding: 4px 0px 4px 4px;
    color: #111418;
}





```
- ```css
.flow-mode .roam-article>div:first-child .rm-block-main.rm-block__self:hover {
 box-shadow: inset 16px 16px 12px 0 #9E9E9E(17 177 19 / 6%),  -3px -3px 6px 0 #fff;
  
}
```
- block 搜索框
    - ```css
.rm-autocomplete__results {
    background-color: #ede9fe !important;
    border-top: var(--bt-elevation);
    border-right: var(--br-elevation);
    border-bottom: var(--bb-elevation);
    border-left: var(--bl-elevation);
    border-radius: var(--bd-elevation);
    box-shadow: var(--sd-elevation);
    --webkit-box-shadow: var(--sd-elevation);
    color: var(--co-elevation) !important;
    font-family: var(--ff-elevation);
    font-size: var(--fs-elevation);
}```
- 修改引用样式
    - ```css
.rm-mentions .rm-ref-page-view .rm-title-arrow-wrapper {border-style:outset;  
font-family:简宋!important;
border-width:2px;
Background-color:#03A9F444;
                                                       }```
- ```css
:root {
    --main-font: "Kaiti SC", "楷体", KaiTi, "楷体_GB2312", serif !important;
}

/* 主要内容区域 */
.roam-body,
.roam-block,
.rm-block-text,
.rm-title-display,
.rm-reference-item,
.rm-level1,
.rm-level2,
.rm-level3,
/* 编辑状态的文本 */
.rm-block-input,
.dont-unfocus-block,
.rm-block__input,
.rm-block__input--active,
div[contenteditable=true],
div[contenteditable=true]:focus,
textarea,
textarea:focus,
.bp3-input,
.bp3-input:focus,
/* 标签相关 */
.rm-page-ref,
.rm-page-ref-link-color,
.rm-page-ref-tag,
.rm-tags-wrapper,
.tag[data-tag],
.rm-hashtag {
    font-family: var(--main-font) !important;
}

/* 确保编辑器中的字体 */
.CodeMirror,
.CodeMirror-line,
.rm-block__input > span,
.rm-block__input--active > span {
    font-family: var(--main-font) !important;
}

/* 侧边栏 */
.rm-sidebar-outline {
    font-family: var(--main-font) !important;
}

/* 页面标题 */
h1, h2, h3, h4, h5, h6 {
    font-family: var(--main-font) !important;
}```
- ```css
/*设置卡片模式下卡片的颜色和背景阴影的颜色，我花了很多时间才学会*/
.flow-mode .roam-article>div:first-child .rm-block-main.rm-block__self {
    width:12.7cm;
    height: 7.6cm;
    margin: 20px;
    box-shadow:8px 8px 16px 0 rgb(16 22 26 / 50%), -8px -8px 16px 0 #fff0;
    border-radius: 0px;
    background-size: 100% 100%;
    background-position: 0px 2px;
    background-image:url(https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2F9d28jUaTRF.jpg?alt=media&token=d238cc32-e9a5-4263-a24e-e1b5d1e9f178
  )!important;
    padding: 20px 16px 16px 0;
}
```
- ```css
.flow-mode .roam-article>div:first-child .rm-block-main.rm-block__self:hover {
 box-shadow: inset 16px 16px 12px 0 #9E9E9E(17 177 19 / 6%),  -3px -3px 6px 0 #fff;
  
}```
- ```css
/*设置卡片模式下卡片的颜色和背景阴影的颜色，我花了很多时间才学会*/
.flow-mode .roam-article>div:first-child .rm-block-main.rm-block__self {
    width:12.7cm;
    height: 7.6cm;
    margin: 20px;
    box-shadow:8px 8px 16px 0 rgb(16 22 26 / 50%), -8px -8px 16px 0 #fff0;
    border-radius: 0px;
    background-size: 100% 100%;
    background-position: 0px 2px;
    background-image:url(https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2F9d28jUaTRF.jpg?alt=media&token=d238cc32-e9a5-4263-a24e-e1b5d1e9f178
  )!important;
    padding: 20px 16px 16px 0;
}
```
- ```plain text
笔记中包含光标时，卡片的样式*/
div.rm-level-0 > .roam-block-container.rm-block.rm-block--mine.rm-focused.block-bullet-view,
div.rm-level-0 > .roam-block-container.rm-block.rm-block--mine.rm-not-focused.block-bullet-view:focus-within {
background-color: #F2E9E96D;
 border-radius:10px;
  box-shadow:8px 8px 16px 0 rgb(16 22 26 / 50%), -8px -8px 16px 0 #fff0!important;
    margin: 10px 20px 10px 20px;
    padding: 10px 0 10px 0;
}

```
- ```plain text
/* 笔记处于行选中状态时，卡片呈现的样式 */
div.rm-level-0 > .roam-block-container.rm-block.rm-block--mine.rm-not-focused.block-bullet-view.block-highlight-blue {
background-color:;
  border-radius: 10px;
 margin: 10px 20px 10px 20px;
  padding: 10px 0 10px 0;
  box-shadow: rgba(60, 64, 67, 0.3) 0px 1px 2px 0px, rgba(60, 64, 67, 0.15) 0px 2px 6px 2px;
} 
```
- ```html
.rm-level-0 > .roam-block-container.rm-block.rm-block--mine.rm-not-focused.block-bullet-view:not(.block-highlight-blue) {
    /* 调整便签的外观 */
    background-color: #8BC34A00!important;
    padding: 15px 20px;
    position: relative; /* 设置为relative，以便之后的图钉样式可以正确定位 */
    border-radius: 5px; /* 为便签增加轻微的圆角 */


    /* 为便签增加阴影效果 */
    box-shadow: 2px 2px 8px rgba(0, 0, 0, 0.1);
}
```
- ```plain text
/* card-list-mode 卡片之间设置空隙 */
div.rm-level-0 > .roam-block-container.rm-block.rm-block--mine.rm-not-focused.block-bullet-view:not(.block-highlight-blue) {
    background-color: #F2E9E96D;
    border-radius:10px;
  box-shadow:8px 8px 16px 0 rgb(16 22 26 / 50%), -8px -8px 16px 0 #fff0!important;
    margin: 10px 20px 10px 20px;
    padding: 10px 0 10px 0;
}

```
- ```css
/*设置左侧边栏背景色*/
.roam-body .roam-app .roam-sidebar-container {
     background-color: white;
}

#roam-right-sidebar-content {
    overflow: auto !important;
}
/*修改笔记主题的字体*/
div {
    font-family: !important;
}

.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .log-button:hover {
    color: #F5F8FA;
    background-color: #FF9800A5;
}

.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .starred-pages-wrapper .starred-pages .page:hover {
    color: #F5F8FA;
    background-color: #FF9800A5
}


.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .top-row:hover {
    background-color: #FF9800A5;
}
```
- 修改顶部图片
    - ```plain text
/*修改最顶端栏目的背景*/
.rm-topbar {
   background-image:url(https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FLdvi6J-jSG.png?alt=media&token=072a0a85-a788-4d5b-949e-547cdee0288d);
  background-position:top; /* 将图片的底部对齐到容器的底部 */
  background-repeat: no-repeat; /* 防止背景图片重复 */
    background-size:120%;
    
}```
- 修改背景图片
    - ```html
/*设置笔记主题的背景色和背景图片*/


div.roam-app>div.flex-h-box>div.roam-main>div.roam-body-main {
     background-size:100% 100%;
   background-image: url(https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FLdvi6J-jSG.png?alt=media&token=072a0a85-a788-4d5b-949e-547cdee0288d);
}```
- 分列效果
    - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FaPcxSe5o-k.png?alt=media&token=d3ab6a1d-503a-4633-ad8e-c8a5f09f5d06)
- 标签样式
    - ```css
/* FLEETING NOTES */
span[data-link-title="Fleeting Notes"]
{ background: #2d303c;
  background-size: 100%;
  color: #6bcc77;
  padding: 2px 5px 2px 5px;
  font-size: 13px;
  line-height: 1em;
  font-weight: 500;
  border-radius: 5px 5px 5px 5px;
  border-style: solid;
  border-color: var(--ls-link-ref-text-color);
  border-width: thin;
  position:relative;
}
span[data-link-title="Fleeting Notes"] .rm-page-ref__brackets {
  display: none;
}
span[data-link-title="Fleeting Notes"]::before {
  background-color:                 #6bcc77;
  content:                          "";
  display:                          inline-block;
  position:                         relative;
  bottom:                           -2px;
  left:                             -2px;
  margin:                           -13px 2px 0px 0px;
  width:                            1.1rem;
  -webkit-mask-box-image:           url("data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABACAYAAACqaXHeAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAAB2AAAAdgB+lymcgAAABl0RVh0U29mdHdhcmUAd3d3Lmlua3NjYXBlLm9yZ5vuPBoAAAQ7SURBVHic7Zvbi01RHMc/DBlEGJchcsnlQUJTo1wGcUhCuTzgxYOU/AHePCGv8qQpbx5QihdxXIZIJiJyaUJEqHFnmIyZ8fBbq7PPvq69Z885++Jbq7X3uq/f/q3v+q3fWQf+I98YUOH+bgDDDMotBzoM2xwONAEtwO9ow6ocfgC9BmGkTxs1QAOwHygCnarO2igDGhSlUgxoAn65pF9Hvqgds4ACsBpYCYxyKVMALoYdSLUE8ADRBju6VTwW+aKrgTXANFu5l8BlFXqBM6ps4qGXwAiP/G8qv4fyJdEOnAJ24xRGLcIXPcCE2EccM0wF0AXcRNZ5AzAwoN2Lqt72sAMK2gVaDToPg4WqvZG4L4FvKu8p7hzhhSnAeOA98M4lfy3wKdRIFboxY+2wIUgD4g71XhM0JcFGZI31Ff1hB/jhEjCmLw1oDaiJYTBgzgF+dkAYfCAmDYgb5yhteVaYaEesqJYAVlapXwfsAhgELKJkdcW5AwBsxGw5hdkBYsFs4DzwHXcWjYsDKo1ADtCop2R9PQOOAZuInwQrDWMBADxUhVdY0jIvACsHFIF5yPpvCWj4AtUjUD9sRbbSSFiHSOuOJc1LA/7QPxZbX8M42zhDacANNbEGYDTwxasSIqxKe5NMEPnra7QgEtus3jPPAfZ9vqjiQn+NKGmwE1kROEiwdyWTJAii6p8QtZlOzkgQNeEWhAP8tCCzJAiwF5HaKXJAgm6YqSp9JAcCcCOy58ArnN5XKzJLghrN+J8G00aCTV4T9fqKRcQH74W0kWABsXSNUUe5RzjtHHA7SuV7ZEcAf5HzjQN+Lq/L/TGiKqEGcbU74CeAok9eGhH6fFNLyU2W9iXQC7RFaSArhlCXiqfaC8Tt9k4q7qrYcb7JiwA0oYe+RJGVJdCk4nZsHz0vGtCGnG/GAvOtGXkRAMBVFZctgzwJwNXfmcQjrQnO4n3HwAqr+XsFsWuWIjZOp0lHSSVB7bc0Ddohcl+9r9INpVUDNLYgv2jbsRPY5ZJeBBYgy+CKSQdJ14A6l7z1lCw/PX6tAQX1rg2jzJHgYuA0otmHkH1fYyIwQz0vRLbEQKRJA+Za0psRj5U2hNpw8sIWk47SIoDJwGuVdp4St1lPgx0IB+jbp0YuvTQIoA54ot6vA0Mt5bQANgCDo3SUdAFMBm6p50c43V6RfhixIukCuKnil8Akl3KZF4A+4c3xKBfbTdFW1VBSYL1K2wWc9CgXeE84iAm7yYatMBHRBgeCNKDRJW0NcBi5TLXPoPMhwBLkGLqMcpYG+AxcQ7w29zC7lT6NcB/ma4iygZiEDPI73lvLDGAPYpXZ/wPQhZiiRxChRNqeqo3HyGSWqfd6YBtwHHiL0+p6ofK2Ed9V+KriKDKxVuRqrX3Cb4ATwA5S8EemKNhA+YR/EsHMTDNGIGbnAeQElna/wn/kFv8A8zvyPfywxCQAAAAASUVORK5CYII=");
  height:                           1.0rem;
} 

/* Literature Notes */
span[data-link-title="Literature Notes"] { 
  background: #2d303c;
  background-size: 100%;
  color: #6bcc77;
  padding: 2px 5px 2px 5px;
  font-size: 13px;
  line-height: 1em;
  font-weight: 500;
  border-radius: 5px 5px 5px 5px;
  border-style: solid;
  border-color: var(--ls-link-ref-text-color);
  border-width: thin;
  position:relative;
}
span[data-link-title="Literature Notes"] .rm-page-ref__brackets {
  display: none;
}
span[data-link-title="Literature Notes"]::before {
  background-color:                 #6bcc77;
  content:                          "";
  display:                          inline-block;
  position:                         relative;
  bottom:                           -2px;
  left:                             -2px;
  -webkit-mask-box-image:           url("data:image/png;base64,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");
  margin:                           -13px 2px 0px 0px;
  width:                            1.1rem;
  height:                           1.0rem;
} 

/* Reference Notes */
/* The text *after* is not as important */
span[data-link-title="Reference Notes"]{ 
  background: #2d303c;
  background-size: 100%;
  color: #6bcc77;
  padding: 2px 5px 2px 5px;
  font-size: 13px;
  line-height: 1em;
  font-weight: 500;
  border-radius: 5px 5px 5px 5px;
  border-style: solid;
  border-color: var(--ls-link-ref-text-color);
  border-width: thin;
  position:relative;
}
span[data-link-title="Reference Notes"] .rm-page-ref__brackets {
  display: none;
}
span[data-link-title="Reference Notes"]::before {
  background-color:                 #6bcc77;
  content:                          "";
  display:                          inline-block;
  position:                         relative;
  bottom:                           -2px;
  left:                             -2px;
  margin:                           -13px 0px 0px 0px;
  -webkit-mask-box-image:           url("data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAgAAAAIACAYAAAD0eNT6AAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAAN1wAADdcBQiibeAAAABl0RVh0U29mdHdhcmUAd3d3Lmlua3NjYXBlLm9yZ5vuPBoAACAASURBVHic7N13tF5F2f7x70WVDiJI7yAQeq9KkN4E6UVpYkBQERGlKGCXbsFXfqJSFEFQEZBOqFJEuvRmaEEjLZAEQpL798dMzCEk5JTn2ffsve/PWmed+K53MdfZZ5899zMze0ZmRgihXiTNDCwCzAnM0eN7X/8N8CYwMn+f/N/T+t8jgRfNbEw3f94QQucpCoAQyiVpfmD5/PWxHv9eApjOL9l7GDAMeBx4LH89DjxmZsM9g4UQpi4KgBCcSZoRWJopd/RzO0brhJGkYmDy4uBJM3vHM1gIbRcFQAgVkjQTsB6wKbAGqbNfCpjBM5eDCcC/SAXBA8BQ4G8xlRBCdaIACKGLJE1P6ug/Ser0NwRmdQ1VrneA20nFwA3A3WY2zjdSCM0VBUAIHSRJwCAmdfifAOZyDVVfbwI3M6kgeMjigRVCx0QBEMIASVqa1Nl/EhgMzO+bqLFGMKkYGGpmTzvnCaHWogAIoY8kzQBsDXya1PEv5puotYaRioG/AFeZ2bvOeUKolSgAQuglSasC+wF7EZ/ySzMC+D1wnpnd4x0mhDqIAiCED5Dfw98b2BdY1TlO6J2HgfOA35rZS95hQihVFAAhTCa/qrc9qdPfmva9otcUE4DrgXOBS81stHOeEIoSBUAImaR1SJ3+HsCHneOEznoTuJg0MnBLvE0QQhQAoeUkLQzsQ+r4V3COE6rxL+B80nqBp5yzhOAmCoDQSpLWAI4FdqScPfVD9W4AvmtmN3kHCaFqUQCEVpG0PnAcsI13llCU24DvmNm13kFCqEoUAKEVJG0CfJP03n4IU/N30ojA5d5BQui2KABCo0naivSJf0PvLKFW7ge+B/wxFgyGpooCIDRO3o//U6SOf03nOKHeHiEVAheZ2XjvMCF0UhQAoTEkTQfsBhwDrOwcJzTLk8APgPPjhMLQFFEAhNrLe/PvAxwNLOccJzTbv4AfAb8xs3ecs4QwIFEAhFqTtCXwM2AZ7yyhVZ4HDjezP3kHCaG/ogAItSRpIeB00pB/CF6uBA4zs2e9g4TQV7EBSqgVSdNL+hLwKNH5B3/bAA9LOlrSjN5hQuiLGAEItSFpbeAXwBreWUKYgkeBQ8zsZu8gIfRGjACE4kmaS9LPgDuJzj+UawXgJknnSJrPO0wI0xIjAKFokvYETgMW8M4SQh+8CnwDODs2EgqligIgFEnSssDPgc28s4QwALeTpgUe9A4SwuRiCiAURdLMkk4AHiI6/1B/GwD3SDpF0mzeYULoKUYAQjEkbQj8BljWO0sIXfA88Hkzu9o7SAgQIwChAEq+DtxEdP6huRYFrpT0fUnTe4cJIUYAgitJ8wLnkd6nDn33NvAUMAwYCbzZ43tv/g0wJzBH/urtv5cg7b44c3d/vMa6BdjTzF7yDhLaKwqA4EbSBsCFpE9G4YMNBx7PX4/1+D7MzCZ4BMqfYpcAPpa/lu/x73hrY9pGAHub2XXeQUI7RQEQKpeP6z0S+D4wg3Oc0jxFOou+Z0f/uJmNdE3VR5Lm4v1FwerAUp65CjSBdNzwCV6FXGivKABCpSR9GDgX2M47SyFeAIYCNwBDzewF5zxdJWlxYNMeXwv5JirGjcBeZvayd5DQHlEAhMpIWp805L+YdxZHI0gP+6GkDv9J5zyuJC3PpGJgMPBh30SuXiYVATd6BwntEAVAqISkrwI/ANp2YMpI4GZyhw88FDvDTZmk6YBVScXAJ4GNgdldQ1VvAnAC8L2YEgjdFgVA6CpJ85CG/Lf3zlKhN4FLSG833Gpm453z1FI+XW8wsC+wEzCLb6JKXUdaIDjCO0horigAQtdIWhe4CFjcO0sFxgPXkzr9S81stHOeRpE0B7ArqRjYGJBvokq8RHpV8BbvIKGZogAIXSFpD9In/5m8s3TZP0md/u/ine5qSFoS+Gz+avpbBeOBIWb2K+8goXmiAAgdJ+lQ4Cc0d6fJ/wAXAOeZ2X3eYdpM0kakUYHdSBsUNdXRZvZD7xChWaIACB2VD/I53jtHF0wALgV+DVxjZuOc84QeJM0C7AgcQHMPkToNODIWkYZOiQIgdERewf1T4AveWTpsHOnT/vfN7HHvMGHaJK0FHAfsQPPWCpwHHBgFaOiEKADCgEmaifRg2t07SweNJa1h+KGZPeMdJvSdpFWAY4FdaNZ01BXAbmY2xjtIqLcoAMKA5DPO/wRs4Z2lQ94GzgZOMrPnvcOEgZP0MeAYYC+as/X0bcD2Zva6d5BQX1EAhH7LJ/ldCazjnaUDRgFnASfHdqzNJGkp4BukRYNNeDvlQWArMxvuHSTUUxQAoV8kLQJcC6zgnWWARgJnAqeZ2X+9w4Tuy/fuUcBBwIec4wzUs8DmZva0d5BQP1EAhD7L+7dfS72P8R0LnAKcYmaveYcJ1ZP0UdJiwUOA6Z3jDMS/SSMB93sHCfUSBUDoE0lrk4b9P+KdZQBuAA6NVf0BQNLqwP8B63pnGYCRwA5mdrN3kFAfTVoZG7pM0makA23q2vlPPG1ts+j8w0R5M6cNgIOBuo4GzQlcLelT3kFCfcQIQOgVSeuRPjnP6p2lHyYAPweOM7M3vMOEckmaDziJtFCwjnsIvAtsa2bXeQcJ5YsCIExTnvO/DZjXO0s/3A0cYmb3eAcJ9SFpY1LRuJJ3ln54C9gk7vkwLTEFED6QpIWBa6hf5/86aVfC9eJBGPrKzG4FVge+RnpFtE5mB66UtLR3kFC2GAEIUyVpbuBW6vcp6LfAV83sP95BQv1JWhQ4A/i0d5Y+ehrYIP4OwtREARCmSNKHSK/6beydpQ/+DXwm5j9DN+QFdr8B5vHO0gf3kKYD3vIOEsoTUwDhffLBPhdQr87/JmC16PxDt5jZX0jTAn/3ztIHawJ/lDSjd5BQnigAwpT8HNjJO0QvGfA9YLPYwjd0m5kNAzYCfuydpQ+2AH4jqY5vNYQuiimA8B6SjgdO8M7RS/8F9jGza7yDhPaR9Gng18Bc3ll66RQz+5p3iFCOKADC/0j6POlAnDr4G7CHmb3gHSS0V15p/wdgDe8svfRVMzvNO0QoQ0wBBAAk7Uga+i+dASeTFjZF5x9c5UN4NiBtJVwHp0ja0ztEKEOMAAQkbQRcR/kno70G7Gtml3sHCWFykvYAfkl6D79kY0m7BV7vHST4igKg5SStANwOzO2dZRr+DuyWF2GFUCRJywGXACt7Z5mGN4GPxwmC7RYFQItJmpXUsQ7yzjINFwGfNbOx3kFCmJb8d/UHYFvvLNPwNLCGmY30DhJ8xBqAdvsp5Xf+Z5JO8IvOP9SCmY0GdgTO984yDUsD/887RPATBUBLSdoHOMA7xzScYGaHmdkE7yAh9IWZjSOdKFj6ivvdJQ3xDhF8xBRAC0n6GPAPyl2sNAE4zMzqsrI6hKmS9A3gB945PsDbwLpm9qB3kFCtKABaJu/xfxewineWqRhL2s//D95BQugUSQeS9tiY3jvLVDwGrGVmdTv5MAxATAG0z48pt/N/i/R6UnT+oVHM7FfALqRP2yVannrsAxI6KEYAWiS/p/x77xxT8V9gazP7h3eQELpF0ieAy4A5vbNMxf5mdo53iFCNKABaQtIywL3AHN5ZpuA5YAsze9w7SAjdJmk14Grgo95ZpmA0aSrgUe8goftiCqAFJM1Mei+5xM7/EWCD6PxDW+TNdzYEnvHOMgWzAn+QNIt3kNB9UQC0w2mkc8xL8yzwSTN70TtICFXKZwh8EhjunWUKVgJ+4h0idF9MATScpF2Ai71zTMEIYEMze9I7SAheJK0K3EKZawL2MrNS1wyFDogCoMEkLUWa9y/tvPJRwGAzu9s7SAjeJG1CWhMws3OUyb0JrBlFenPFFEBDSZqOtOK/tM7/XWDn6PxDSMzsJmAf0gZYJZkDuFBSqXsXhAGKAqC5hgDreIeYjAEHmNk13kFCKImZXQJ8yTvHFKwBHOYdInRHTAE0kKT5gMeBebyzTOZIMzvVO0QIpZL0HeA47xyTGQksb2YlLlgMAxAjAM10EuV1/qdG5x/CBzOzbwK/8s4xmTmBU7xDhM6LEYCGkbQhcCsg7yw9/I60v3/cbCFMQ55z/xOwg3eWyQzO6xVCQ0QB0CD5wXEvZe31fw2wvZm96x0khLrIG/FcR9owqBSPAKvF33JzxBRAsxxGWZ3//cAu8cAIoW/MbAywPfCEd5YeVgS+4h0idE6MADSEpAVJR3qWsqFIvEMcwgDljYLuBD7knSUbRVoQ+IJ3kDBwMQLQHKdQTucPMCQ6/xAGxsweAI7wztHDbMDp3iFCZ8QIQANIGgwM9c7Rw9lmdpB3iBCaQtIfgF29c/SwpZld6x0iDEwUADUnaUbSXPuK3lmyfwLr5DnMEEIHSJqLtMB3Ke8s2ZPAymb2jneQ0H8xBVB/X6Gczn80sFt0/iF0lpm9AewOjPXOki0LfM07RBiYGAGoMUmLkBb+zeadJdvfzM7xDhFCU0k6nHLm4McAK5rZv7yDhP6JEYB6O4NyOv/zovMPobvM7AzgMu8c2SzAT7xDhP6LEYCakrQ+cLt3juwxYC0zG+UdJISmk/Rh4D5gMe8s2aZmdqN3iNB3MQJQX6UcGPI2sHt0/iFUw8xeBfYAxnlnyY71DhD6JwqAGpK0GrCNd47scDN70DtECG1iZndQzoeAT0pa1ztE6LuYAqghSRcDu3jnAK4zsy28Q4TQRpIE3AGU0PleZmaf8g4R+iYKgJqRtDzwMP6jN2OBVczsceccoYd8iMyywPL5aynSDpFzALNP4TvAW6Stmyf/PhJ4hrTG4zHgyXjFsyyS1gDuxv95YMCqZvaQc47QBzN4Bwh9djT+f+wAp0bn70vSwsCmwBpM6vAXo+/3x4fz17RMkPQckwqCe4GhZvZiH9sLHWJm90r6BfAF5ygiPZv2cs4R+iBGAGpE0hKkHbi8C7fnSQeCjHbO0SqS5gc2IXX6g4HlXANN8gRwI2k76pvM7D/OeVpF0tzA48D8zlHGk54LTznnCL0UBUCNSPo/4GDvHMDOZvYn7xBtIGll4DPA1sAg0ietkhlpiuoq4PwYEq6GpH2Bc7xzEOeA1EoUADWRj/t9FpjZOco1ZraVc4ZGy5/09wI+C6zuHGeg7gPOAy6IkYHuyQsCbwE2co4yFlg6jguuhygAakLSqfgfCzoWWCmO+e08STMDOwD7AlviP83TaeOAa4BzSSvG4xCZDpO0CnAP/vfOj83scOcMoReiAKgBSfMCw/Df9vd7ZlbKu8eNIGk2YAhwJLCgc5yqDAdOAc6KDaQ6S9LpgHfnOxpYwsxGOOcI01DCavIwbYfj3/kPA77vnKExJM0l6TjSdT2V9nT+kH7WU4Fhko7LR92GzjieVGB5mhX/IiT0QowAFE7SnKROYm7nKDuZ2aXOGWpP0nykI5wPJb2fH9J+A2cCp8enxoGTtCdwgXOMN4DF8zHGoVAxAlC+Q/Hv/K+Kzn9gJM0o6SjSQs6jic6/pzlJ1+RZSUdJmtE7UJ2Z2e9Jr2V6mov07AoFixGAguWFYc8D8znGmAAMMrPHHDPUmqTBpE+4K3hnqYlHgUPjhLn+k7QqcL9zjBHAYmb2tnOOMBUxAlC27fHt/AH+GJ1//0haQNLvSBvkROffeysAQyX9TtIC3mHqyMweAK5wjjEf6c2WUKgoAMr2We8AxMK/PpM0naQvkXZni61R+28v4HFJX5IUz6q+K+Fvt4RnWJiKmAIoVF4s9iLgOR96pZlt69h+7eRNfH4HbOadpWGuB/aOzYT6RtJQ0rbRXsYBC8fvrUxRVZdrD3w7fyjjE0RtSNqENO8anX/nbQbcn69x6D3vv+EZgD2dM4SpiAKgXN5DZzeb2d+cM9RCHvI/jvQptU3v81dtQeD6vHdAPLt6wcyuB/7uHMP7WRamIqYACiRpedJKaE9bmNl1zhmKl4f8fwts7p2lZa4D9omh5WmT9CnA+zXeQWb2iHOGMJmoosvkXTHfHZ3/tEkaRNp7PTr/6m0O3JN/B+GDXUY6odGT9zMtTEEUAIXJp3rt7RzDe96weJI2AG4FFvHO0mKLALfm30WYCkvDvD9wjrF3TNuUJ34h5dkEWMyx/YeBvzi2XzxJ25Lm++fxzhKYh7QuIN5W+WAXAs84tr8Ivm8jhCmIAqA8n3Fu/wcWC0OmStK+pPnUWbyzhP+ZBbg0/27CFJjZeOBHzjFiGqAwsQiwIJJmBV4G5nCK8AywXH5YhMlIOhI4CZB3ljBFBhxlZqd4BylR3lr8GWAhpwhvAQvEEdDliBGAsuyIX+cPcGZ0/lOWO/+Tic6/ZAJOzr+rMBkzewf4hWOE2YGdHNsPk4kCoCyew//j8T9CtEh5aPkk7xyh106K6YCp+i1ppMSL9xRn6CGmAAqRDz15AZjeKcI1ZraVU9vFyovLLiXtaBbqYxywo5n91TtIaSTdCmzk1PwEYFEze8mp/dBDjACUYy/8On+A8x3bLlJ+vexiovOvoxmAi+MVwSny/FufjjggqxhRAJTD8zWmt/DfKawoeYOZK4jV/nU2C3BFbBb0Pn8A3nFsfzvHtkMPUQAUIK/O9fyk8udYmTtJ3t73auI9/yaYB7g6/04DYGavA5c7RlhPUhTWBYgCoAzrAx9ybD+G/7O8W9lviR3+mmQR4LexE917eP7Ne3/gCVn8QZTBc4esl4AbHNsvzTHE3v5NtDnpdxuSq4BXHNvf1LHtkMXipjJ4/jFcYGYTHNsvRj5r/gTnGJ3yLvAsMJxU5L3U4989/2+QNoZZMH/v+e+J35cEZqwwe7ecIOk2M7vJO4g3M3tX0oXAoU4RYlvgAsRrgM7y7n+vATM5RVjNzB5warsYeY74flKnV1dvktYuXApcmed6B0zS3MA2pI2qtsJ3s6qBGk6651t/jLCkdYE7nZofB8xjZm85tR+IAsCdpC2Aa5yaf8jMVnFquxh5bvgaYDPvLP0wnLSg61JgaN7trWvygtVNScXA9tSzYLoe2DJGvkDSE8CyTs1va2ZXOrUdiDUAJfAcCovFf8lh1KvzHwOcQVo8urCZDTGzq7rd+UPaTja3NQRYOGc4I2eqi81Iv/Pg+wyIaQBnMQLgTNJdwDpOzS9iZi86tV2EvAPj48Cc3ll6YQJwDnC8mb3gnOU9JC0CnAjsRz0+WIwEPmZmL3sH8SRpaeApp+bvNbM1ndoO1OMPtbEkzQl4/QE80vbOPzuVenT+VwCrmNmBpXX+AGb2gpkdCKxCylq6OUm/+1Yzs6eBp52aX01S7LXhKAoAXx/Hb/vfoU7tFkPSYMrflvQuYBMz297MHvYOMy1m9rCZbQ9sQspesr3yPdB2Xs+C6YBPOLUdiALAm+fD50bHtt1JmhE40zvHB3ge2NXM1jOzm73D9JWZ3Wxm6wG7kn6WUp2Z74U283wWRAHmKAoAX17v/xtQu06lw74CrOAdYipuB9Yys0u8gwxU/hnWIv1MJVqBdC+0mWcBEBsCOYpFgE4kfRj4LyCH5h8ws9Uc2i2CpPlIm+TM5p1lCs4BhpjZWO8gnSRpJuAs0iLB0owCljSzEd5BvEh6GFjRoWkDPtrma+8pRgD8bIJP5w8tH/4nfeIrrfOfABxpZvs3rfMHMLOxZrY/cCTpZy3JbMQogNczQcQ0gJsoAPxs4th2awsASXPht/3p1IwEtjOzxq9Kzz/jdqSfuSSH5nujrTwXBW/i2HarRQHgx2sHvgnALU5tl+CLlPXa31PAemZ2lXeQquSfdT383j+fkjlJ90Zb3UQajvewqlO7rRdrAJxIGg4s4ND0PWa2lkO77iTNBgwD5vXOkk3s/D1PZXMjaV7SXvTLeGfJXgEWN7NR3kE8SLoXWN2h6VfM7CMO7bZejAA4yEONHp0/tHj4HxhCOZ3/SGCHtnb+APln34FypgPmJd0jbeX1bJg3F4OhYlEA+PiYY9utLADyITZHeufIJgB7mNmj3kG85WuwB+UsDDwy3ytt5LkOwPOZ2FpRAPjwutnHAbc6te1tB8o5ue6oNs35T0u+Fkd558gWJN0rbXQL6RnhIQoAB1EA+Fjeqd17zexNp7a97esdIDunDav9+ypfk3O8c2Sl3CuVys+G+5yajwLAQRQAPrxu9n86tetK0vzAlt45SLvhtXmOeVqGUMaOgVvme6aNHnJqNwoAB1EA+PC62R93atfbXsAMzhmeB3Zq4iY/nZKvzU74nx0wA+UfEtUtXs+IKAAcRAFQMUnTAcs6Nd/WAuCz3gGAI8zsP94hSpev0RHeOSjjnvHg9YxYRpLXyaitFQVA9ZYAvFYZt64AkLQyPu8293RXEw72qUq+Vt5HCa+e75228XpGzAgs5dR2a0UBUD2vBYDjgKed2vb0Ge8AwNe9A9RQCdeshHunak8TbwK0RhQA1fO6yZ81s3ed2va0tXP7V5hZ249e7rN8za5wjuF971QuPyOedWo+CoCKRQFQPa8RgDYO/88PDHKMMAH4hmP7dfcNfDcIGtTStwFiIWBLRAFQvXgDoDqb4HfkMqR3/h92bL/W8rU7xzGCaOdJdY85tRsFQMWiAKie103u9UftaVPHtscAxzu23xTHk66lF897yEuMALREFAAVcj4EqI0jAIMd2z7LzF5wbL8R8jU8yzGC5z3kxetZ8dH8jAwViQKgWos6tt2qAkDSwsByjhEucmy7aTyv5XL5XmoTz2eF5zOydaIAqNYcTu2+3sJNaDyHbofj/x57k9xFuqZeWjUNkJ8Vrzs17/WMbKUoAKrldXO36tN/toZj25ebmTm23yj5Wl7uGMHzXvLi9cyIAqBCUQBUy+vm9t5b3YPX65YAlzq23VSe19TzXvLi9cyIAqBCUQBUy+vmbuMRwF4P7TeBoU5tN9lQ/O7jNhYAXtc6CoAKRQFQrdmd2m1VASBpFmAxp+avNrN3nNpurHxNr3ZqfrF8T7WJ1zPD6xnZSlEAVMurun3LqV0vy+J3b8fwf/d4XVvPEzy9eD0zYgSgQlEAVCumAKrhNWT7LnClU9ttcCXpGnto2zRATAG0QBQA1YoCoBpeD+tnzczr9anGy9fW66CaKACqEQVAhaIAqFZMAVTD61zxl5zabROva9y2s+pjCqAFogCoViwCrMacTu16blbTFl7X2Oue8hKLAFsgCoBqxRRANbyuc4wAdJ/XNW7bJ9OYAmiBKACqFVMA1fD6FBEjAN3ndY3b9sk0pgBaIAqAasUIQDViBKC5YgSgGjEC0AJRAFQrCoBqeH1aiwKg+7yucdtGAKIAaIEoAKrl9RBp2xSA10MkpgC6z+sat61j8npmtK3QchUFQLViBKAaMQLQXDECUI0YAWiBKACq5XW9Jzi1G0KoJ69nRvRJFYqLXa3RTu3O6tSuF6/hy4Wc2m0Tr2vctmk0r2eG1zOylaIAqFYUANXwGr5c0KndNvG6xm2bRosCoAWiAKhWFADViBGA5ooRgGpEAdACUQBUKwqAanh9WosCoPu8rnGMAFQjCoAKRQFQrSgAquH1aS2mALrP6xrHCEA1ogCoUBQA1YoCoBoxAtBcMQJQjSgAWiAKgGpFAVCNkU7txghA93ldY697yksUAC0QBUC1ogCoxjNO7cYIQPd5XWOve8pLFAAtEAVAtaIAqMZjTu0uKWlup7YbL1/bJZ2a97qnvEQB0AJRAFTL6+Zu2/aaXg/rGYFtnNpug21I19hD2woAr2dGFAAVigKgWl4398JO7Xp5Er+tTHd0arcNvK7tBNI91SaLOLUbBUCFogColtfNvZhTuy7MbAzwnFPzW0ma2antxsrXdCun5p/L91SbLOrU7iindlspCoBq/dup3VYVAJnXkO0cwKZObTfZpvgNS7dt+B/8nhlez8hWigKgWsOc2o0CoFoxDdB5ntc0CoDqPO/UbitFAVAtr2HphSVN79S2l3sd295ekhzbb5R8Lbd3jOB5L1VO0nT4rRuKAqBCUQBUy6sAmIH2bVIz1LHtBYF1HdtvmnXxvX897yUPC5KeGR6iAKhQFAAVMrPX8NtTvFXTAGb2IvCEY4TdHdtuGs9r+US+l9rEawHgGDP7r1PbrRQFQPW8RgFaVQBkNzq2PUSS16tUjZGv4RDHCJ73kBevZ8ULTu22VhQA1YsCoDqeQ7ezACc6tt8UJ5KupZe2Df+D3whADP9XLAqA6sWbANW5CTDH9veTNMix/VrL124/xwhGuofaZnGndr0+HLVWFADV87rJW9cRmdl/gIcdI0wH/NCx/br7Ib7PqIfzPdQ2Kzm1GyMAFYsCoHpeBcDqLX017Srn9reT9AnnDLWTr9l2zjG87x0vqzm1GwVAxaIAqJ5XATAXsLRT257O9w4A/Mg7QA2VcM1KuHcqJWkJYB6n5qMAqFgUANXznOda07FtF2b2EHCfc4x1Je3inKE28rXy3kfhvnzvtM3qjm1HAVCxKACq9wIwzqntNZza9XaedwDgNEnze4coXb5Gp3nnoIx7xoNXAWD4LZBurSgAKmZm4/BbmNa6EYDsAvyKrokWBf4saSbnHMXK1+bP+L2GNtE40j3TRl4FwFNm5rVJWmtFAeDDa2/xVo4A5JXc13jnADYAzvIOUbCzSNfI2zUtXf0PfgVAq85bKEUUAD68bvZ5JC3p1La3c70DZPtJ+qp3iNLka7Kfd46slHulUpLmw+8QoHuc2m21KAB8eN7sbZ0GuAwY7h0iO0nS1t4hSpGvxUneObLhpHuljTwXAMYIgIMoAHw8AIx3arut0wDvAKd458imAy6UtIJ3EG/5GlxIOc+iU/K90kZRALRMKX90rWJmo4HHnZovYY7Vy1nAK94hsjmByyTN6x3ES/7ZLyNdixK8QrvXaHhtWPWvfFJqqFgUAH68pgE2kDSHU9uuzGwUcIZ3jh6WAe5s40hA/pnvJF2DUpyR75HWkTQzfgVAzP87iQLAj9eQ14zAYKe2S/BTYKR3iB4mFgGtWROQf9bSnS1JLgAAIABJREFUOv+RpHujrTYGZnVqO4b/nUQB4Mfzpt/SsW1XZvYGcKZ3jsnMCVzRhrcD8s94BeUM+090Zr432srzmRAFgBOZeZ6W2l55GP4NwOOAnqfNrKRPX5XKrzs9C8zmnWUKzgGGmNlY7yCdlDf5OYtyXvXraRSwpJmN8A7iRdIDwCpOzc/f5mvvKUYAnJjZm8CTTs0vLam1BUB+2HzbO8dU7Afc2KRtg/PPciNldv4A325zByRpQfw6/xfafO29RQHgK6YB/JwOPOodYio2AP7RhAOE8s/wD8p9++RR0r3QZls4th3D/46iAPB1u2PbrS4AzOxd4FDvHB9gUeBiSXdK8lqd3W+SPiHpTuBi/Pf2/yCH5nuhzTyfBTc5tt16UQD4utqx7cGSZnRs352Z3Uj5h76sC9wk6XJJg7zDTIukQZIuJz3YvY/0nZYL8j3QWpIEbO4Y4VrHtlsvFgE6k/QM4LU//2Azu8mp7SJIWoC0KVNpq9KnZAJpkeDxZvaCc5b3kLQIcCJpnr8OHyxGAh8zs5e9g3iStBZwt1PzL5rZIk5tB+rxh9p0nqMA2zu2XYTcAXzTO0cvTQccADwh6XRJ6+VPcC6UrCfpdOCJnK0uz5Rvtr3zz3ZzbDs+/TuLEQBnkj4FXOrU/HBgUTPzOpegCJKmIx0XvJl3ln4YDlxOuoeGdnsf+7xj3KbAjqQCcsFuttcl1wNbmtkE7yCe8n0/DPD6FL6nmV3o1HYgCgB3eT+AV0g79HnYysyucWq7GPlVtfupZ4c20ZukEaVLgSvN7PVO/EclzQ1sQ+r0twLqvJX0cGA1M/uPdxBvkjYFbnBqfgLp/f9SzuZopSgACiDpJvz24b7AzPZ2arsokjYhfTqc3jlKJ7xL2uxoOPBS/ho+2feX8v/vQqTCZ6HJ/j3x+5L4FaidNB7YrO3rXiaS9CvStI2Hf5jZ2k5th2wG7wABSJ/avAqAHSXNkTcmajUzu0nSCcB3vLN0wIzAcvkrJCdE559I+hDguc9E60cdS1CXBTtN5/nHMCuws2P7pfk+cJ13iNBx15F+tyHZHt83X2IBYAGiACjD/cC/Hdv/rGPbRckLw/YBinrNLgzIC8A+bV/0N5l9HNt+E7jDsf2QRQFQAEsLMTwr4k0kLebYflHyArGtgNe8s4QBe4200LX1i/4mkjQv4Hn89I2x+2IZogAoh+c0gIBYCNiDmT0MbAeM8c4S+m0MsF3+XYZJdsN3UWcM/xci3gIohKSPkFZney3MfMzMVnBqu1iStiW9VhcLZutlHLCjmf3VO0hpJN0FrOPU/ARg8dJ2smyrGAEohJn9F99RgOUlbezYfpFyB/I5ICrl+jDgc9H5v5+kDfDr/AFuis6/HFEAlOV85/a/5tx+kczsXOAo7xyh147Kv7Pwfkc6t+/9jAs9xBRAQfK7uS8DczlFMGCQmT3q1H7RJB0JnERaMxHKY6TO/xTvICWStAzp4CuvD35jgI/GniPliBGAgpjZ28AljhGE/yeEYuWOZX/S/HIoyzhg/+j8P9BX8H3m/yU6/7LECEBhJH0cuNkxwlhgCTMb7pihaHlh4MXALN5ZApA+We4ac/5Tl1/9e4608ZeX7eJ3VJYYASjPrcC/HNufCfiyY/vFyw+xzYh9AkrwGml//+hYPtgX8O38RxDb/xYnCoDC5E2Bfusc42BJntuEFs/Mbgc2JnYM9PQCsHH+XYSpyEc4H+Yc4/dmFlNnhYkCoEzeK2XnAj7vnKF4eYOZNYmzAzxcB6wZm/z0ymeA+Z0zeH+oCVMQawAKJelOYF3HCC8CS8aWndMmaTrgGOAEmnGUcMnGk67z92Nv/2mTJOBhwHOTr8fNbHnH9sNUxAhAubxHARYG9nLOUAtmNsHMvktaFxCLJ7tnOGm+/7vR+ffaXvh2/hCf/osVIwCFyqt2h+O7Z/ezwPJmNtYxQ61Imh/4HakYCJ1zPbB3HOrTe3nu/3FgcccYBixlZv9yzBCmIkYACmVmrwCXO8dYEviic4ZayR3UlqQ3KUY6x2mCkaRruWV0/n12GL6dP8Bfo/MvV4wAFCzv2/035xivAcuY2avOOWpH0gLAqcRUSn9dAHzVzF72DlI3kuYBngbmcY4y2Mxucs4QpiJGAAqWX2/yfsVpHuCbzhlqycxeNrO9gU2B2F659x4FNjWzvaPz77dj8O/874nOv2xRAJTvZO8AwKGSlvYOUVdmdiOwKvB1YJRznJKNIl2jVfM1C/0gaTHKmLqLbZkLF1MAhcuvmD0KLOcc5RIz29U5Q+1Jmo+0J/uhQGy2lIwEzgRON7MR3mHqTtL5wD7OMYaRpg5j85+CxQhA4fLrTqd65wB2yWsSwgCY2QgzOwZYjDS18opzJE+vkK7BYmZ2THT+AydpNWBv7xzAGdH5ly9GAGogHxM8DP/dvO40s/WdMzSKpNmAIaRTGBd0jlOV4aTh4bPMLKZEOkjStcDmzjFeBxY1s7ecc4RpiBGAGsjHBP/UOwewnqTdvEM0iZmNMrPTSK9c7gb8lWYeNzyO9LPtRtph8rTo/DtL0q74d/6QCrvo/GsgRgBqQtKHScd5zuYcZRiwcpzr3T15M6G9gM8CqzvHGaj7gPOAC+I9/u7JG4c9gv8o4buk48Rfcs4ReiFGAGoiv4f/a+8cpI1FSngzobHM7D9mdoaZrQGsQrre/yTtqlY6I2U9GVjFzNbIP0t0/t11Bv6dP6RT/6Lzr4kYAagRSUsAT+F/4IwBm5vZDc45WiWPDGxC2ldgMP5vhkz0BHAjMBS4KTr7aknaFrjCO0e2qpk96B0i9E4UADUj6ffAHt45iKkAd5IWJhUDawDL56/F6N7I3gTSNNRj+eteYKiZvdil9sI0SJqTdNrfIt5ZSNv+bucdIvReFAA1I2kV0rxqCdM3Z5nZwd4hwiSSZgGWZVJBsBRpv4E5gNmn8B3gLeDNKXwfCTzDpA7/STMbU9XPEqZN0i9Ib5F4mwCsZmYPeQcJvRcFQA1J+jWwv3cOYiogBDeSBgM3APLOAvzGzA7wDhH6JgqAGpK0EPAkMKt3FmIqIITKSZoVeBAoYYvuMcCyMRVUPyUMI4c+yqtsS9gdEOKtgBA8fIcyOn9IWzhH519DMQJQU5JmJ40CLOCdhZgKCKEyktYC7sT/bSCAEaQ9/0d6Bwl9FyMANZV32vqWd45MwK8lzeUdJIQmkzQDcDZldP4A34nOv76iAKi3X5NeASrBYsTxnyF025Gko6VL8BTwC+8Qof9iCqDmJG0NXOmdIzNgsJnd7B0khKaRtAzwEPAh7yzZrmZ2iXeI0H9RADSApOuAzbxzZE+QdgN72ztICE0iaShpB8gSxMmgDRBTAM1wJGkjjhIsRzrjPYTQIZIOoJzOH+Br3gHCwMUIQENI+g2wn3eO7F1gzdgVLISBk/RR4FFgHu8s2R/NbBfvEGHgogBoiLwv/GNM2t7V213ABmZWyshECLUk6SJgN+8c2evAimY23DtIGLiYAmiIvBFHScNy6wKHeYcIoc4kbUc5nT/AEdH5N0eMADSIJAHXk06IK8FbwCAze847SAh1I2kO0mu+i3pnya41sy29Q4TOiRGABrFUzR1I6nhLMDvwc+8QIdTU9ymn838L+Lx3iNBZUQA0jJn9C/i6d44etpW0u3eIEOpE0nrAF7xz9HC0mQ3zDhE6K6YAGihPBQwFNnGOMtF/gBXM7FXvICGUTtKMwH3AIO8s2W3Axy06i8aJEYAG6jEVMMo7SzY/sU1wCL31Dcrp/N8GDozOv5miAGgoM3sGONo7Rw/7SyplcWIIRZL0MeBY7xw9HG9mT3iHCN0RUwANlqcCbgI+7hxloqeAlWOb4BDeL/+93gxs7J0l+wewnpmN9w4SuiNGABosD9sdAIz2zpItAxzvHSKEQn2ecjr/d4EDovNvtigAGs7MngaO8c7Rw5GSSjnONIQiSFoI+JF3jh5+GFt5N19MAbSApOmAW4ANvbNkdwPrx6eLEBJJfwQ+7Z0jewxYzcze8Q4SuitGAFog78d/EDDWO0u2NvAl7xAhlEDSTpTT+RtwUHT+7RAFQEuY2aOkncVK8R1Ji3uHCMGTpLmAn3nn6OEsM7vNO0SoRkwBtIikmUgbjKzonSW72sy29g4RghdJvwCGeOfIXiJt2DXSO0ioRowAtIiZjSVNBZRS9W0laS/vECF4kLQRZe2vf2h0/u0SIwAtJOlMytlnfATpU8cr3kFCqIqkmYH7geW9s2R/NLNdvEOEasUIQDsdDbzoHSKbDzjVO0QIFTuWcjr/N4AveocI1YsCoIXyMN+h3jl62FfSZt4hQqiCpEGUdWLn18xsuHeIUL2YAmgxSZcAO3vnyJ4BVjKzMd5BQuiWvCfHbcD63lmyW4BN4rCfdooRgHb7IvC6d4hsKeBE7xAhdNkXKKfzf4f0zn90/i0VBUCL5WG/koYivyJpde8QIXSDpEUobC+OOOmv3WIKoOUKPDHwHmDd2CY4NI2ky4DtvXNkDwFrmtm73kGCnxgBaLk8/Pd50nBgCdYEDvcOEUInSdqNcjr/CaSh/+j8Wy4KgICZPQ581ztHD9+WtKR3iBA6QdI8wE+8c/TwUzO7yztE8BdTAAEASTMC9wIreWfJrjWzLb1DhDBQks4GDvTOkT0HDDKzt7yDBH8xAhAAyMOBB5GGB0uwhaR9vEOEMBCSBlNO5w9wSHT+YaIoAML/mNmdwJneOXo4XdJHvEOE0B+SPgSc5Z2jh9+b2ZXeIUI5ogAIkzsWeN47RPYR4HTvECH007eAZb1DZK8CX/YOEcoSBUB4DzN7k3IOCgLYR9IW3iFC6AtJqwBf887RwxFmNsI7RChLLAIMUyTpImA37xzZs6Rtgkd7BwlhWvJ2v3cCa3tnya43s829Q4TyxAhAmJovAa95h8iWBL7tHSKEXvoS5XT+o4Eh3iFCmaIACFNkZv+mrCHMwyWt6R0ihA8iaXHK2lPjeDN7xjtEKFNMAYQPJGkoMNg7R3YfsI6ZjfMOEsKUSLoK2Mo7R3Yv6e8lttUOUxQjAGFahgBve4fIVgeO8A4RwpRI2otyOv/xwOei8w8fJAqA8IHM7EnKmn8/QdJS3iFC6EnSvMAZ3jl6OM3M7vMOEcoWUwBhmiTNQDqlbxXvLFmsag5FkXQu8FnvHNkzpLdmxngHCWWLEYAwTXnOvaRtgjeTtK93iBAAJG1OOZ0/wJDo/ENvRAEQesXM/g781DtHD6dKms87RGg3SbMCv/DO0cM5Zna9d4hQD1EAhL44FhjmHSIrbc41tNOJQClrUv4DfNU7RKiPKABCr5nZKOAQ7xw97CVpa+8QoZ0krQF8xTtHD182s1e9Q4T6iEWAoc8kXQDs6Z0jG0Y633yUd5DQHpKmB+4mvZpagivNbFvvEKFeYgQg9MfhpNPFSlDazmuhHY6gnM7/LcoamQs1EQVA6DMzK22u8YuSStl7PTRc3ofiRO8cPRxrZs95hwj1E1MAod8kXQ980jtH9gCwVmwTHLpN0nXAZt45sruADcyslFd0Q43ECEAYiCFAKe8brwoc6R0iNFvef6KUzv9d0na/0fmHfokCIPSbmT0NnOCdo4fjJS3jHSI0U9534jTvHD38yMz+6R0i1FdMAYQBydsE3w2s5p0lG2pmpUxLhAYp7O2Xx4FVzewd7yChvmIEIAxInnP/HOn0sRJsKml/7xChWfJ+E6V0/gZ8Pjr/MFBRAIQBM7N7gB975+jhVEnze4cIzSBpduD/vHP08Eszu8U7RKi/mAIIHZH3RH8YWMI5ykQXmdke3iFC/Uk6A/iyd45sOLCCmb3hHSTUX4wAhI4ws9HAwd45ethdUuyMFgZE0jrAF71z9HBYdP6hU2IEIHSUpPOBfbxzZM+Rtgl+yztIqB9JMwL/AFbxzpL92cw+7R0iNEeMAIRO+wrwX+8Q2WLA97xDhNr6GuV0/m8Ah3mHCM0SIwCh4yR9BjjPO0c2gbRT2l3eQUJ9SFoWeBD4kHeW7GAzO8s7RGiWKABCV0i6BtjCO0f2ELCmmb3rHSSUT5KAocAmzlEmuhX4hMXDOnRYTAGEbjkYGO0dIluZNJwbQm8cSDmd/zukd/6j8w8dFwVA6Aozexb4lneOHr4paTnvEKFskhYATvbO0cP3zOwx7xChmWIKIHSNpOlJp5Wt6Z0luxkYHJ+mwtRIuhjYxTtH9jCwekxdhW6JEYDQNWY2HjgIKOWI3k+QhndDeB9JO1BO5z+BdNJfdP6ha6IACF1lZvcBp3vn6OHkPMwbwv9ImgM40ztHD2ea2Z3eIUKzxRRA6DpJswD/BJbyzpJdbGa7eYcI5ZB0JvAF7xzZ88CKsYFV6LYYAQhdZ2ZjgCHeOXrYVdL23iFCGSRtABzinaOHQ6LzD1WIEYBQGUnnAPt658heIH3KetM7SPAjaSbgPmBF7yxZHGIVKhMjAKFKXwVGeIfIFgF+4B0iuDuacjr/V4EveYcI7REjAKFSkvYCfuedI5sAbGRmd3gHCdWTtAJwPzCTd5bsADP7jXeI0B5RAITKSboS2No7RxbvWrdQ3u73VmBD7yzZUDP7pHeI0C4xBRA8HAKM8g6RDQK+4R0iVO5gyun8xwCf9w4R2icKgFA5MxsGHOedo4djJX3MO0SohqSFgR965+jhBDN72jtEaJ+YAgguJE0H3Ams7Z0lixPXWkLSn4EdvXNk9wNrm1kpu2WGFokRgODCzCZQ1jbBG5PyhAaTtDPldP7jSdv9lvI3EFomCoDgxsweAE7xztHDSZIW9A4RukPSXMBPvXP0cIaZ3eMdIrRXTAEEV5I+BDwELOOdJfuTme3sHSJ0nqSzKGex3bPASmY22jtIaK8YAQiuzOxtynkoA3xaUilDxKFDJH2csqZ4hkTnH7xFARDcmdmNwK+9c/TwM0lzeocInSFpZuD/AfLOkp1nZtd5hwghCoBQiiOBf3uHyEp7TSwMzHFAKa95jgCO8A4RAsQagFAQSbsDF3rnyAzY2Mz+5h0k9J+klYB7gRm9s2R7m9kF3iFCgCgAQmEkXQ5s550jexRYzczGegcJfZf3mrgdWNc7S3a1mZWyBXYIMQUQivMFoJSz0FcgnRYX6ulQyun8R5G2Hw6hGFEAhKKY2fPAMd45ejgmnxoXakTSosD3vXP0cFzeAjuEYsQUQChOgUO3fyOtB4g/lpqQdAWwrXeO7O/A+nn3yxCKESMAoTj5Qfk5oJQjejckhm9rIy8mLaXzfxc4KDr/UKIoAEKRzOyfwEneOXr4YT5FLhRM0oeBn3jn6OFkM3vQO0QIUxJTAKFYeQOXB4HlvLNkl5rZTt4hwtRJ+jWwv3eO7Alg1bzbZQjFiRGAUCwze4e0TXApVeqOkj7tHSJMmaRNKafzN+Dz0fmHkkUBEIpmZjcDZ3vn6OFn+VS5UBBJs5C2+y3Fr/K9G0KxogAIdXAU8LJ3iGxBylqbEJLjgaW9Q2QvA1/zDhHCtMQagFAkSTMAywOr5K+dKGctgAGfMLNbvYMEkLQacDcwg3eW7Angz6T1Kw8Cj5tZKW+0hPA/UQAEd5IWYFJHP/FrBWAmz1zT8Bhpm+B3vIO0maTpgbuANb2zfICxpG2lH+z5ZWaljGqFlooCIFQmr+pfkfd39vN75hqA75jZt7xDtJmkI4BTvXP00wgmKwqAR2LhYKhKFAChK/JWrJN39MtRzjBtJ7wLrG5mD3sHaSNJSwAPA7P6Jumo8aQphMlHC55zTRUaKQqAMGCSZiQNwW6UvzYEPuIaqjp3ABvFTm/Vk3Q1sKV3joq8StqS+lbgNuCeOKUyDFQUAKHPJM0JbMCkDn8dYBbXUL4OM7MzvUO0iaR9gPO9czgaQzpj4DZSUXCHmY30jRTqJgqAME2SFmFSZ78RsDLxCmlPbwIrmtkL3kHaQNJHSIvq2jLK1BsTgAdIBcFtwK1mNtw3UihdFADhPSSJtFBvI2Dj/H1x11D1cLmZ7eAdog0knQ/s452jBp5h0pTBbWb2mHOeUJgoAFour8xfi/fO38/jGqq+djOzi71DNJmkLYGrvXPU1Ajeu47gXjMb5xspeIoCoIUkrQ7sAGwGrA3M7JuoMV4GVjCz172DNJGkWUmr/pdwjtIUo4E7gRuAy/IJnKFFogBogbxK/xPAp0gd/2K+iRrtbDM7yDtEE0k6FTjCO0eDPQNcBvyFNGUQowMNFwVAQ+UDa7YmdfpbA3GATTUMGBwHwXSWpLVIn1an987SEq8BfyUVBFeb2ZvOeUIXRAHQIHnznYmf8jcBZnQN1F5xDnwH5XMh7gZW887SUmOBG0nFwGXxtktzRAFQc/kglE/lr9Wd44RJvmdmx3mHaAJJXwd+6J0j/M+9pGmCy8zsfu8wof+iAKiZmM+vjXeBNc3sIe8gdSZpGdJ2uG3eaKpkzzFp3cDNcephvUQBUAM95vN3ALYh5vPr4i5gg9gmuP8k3QBs6p0j9MobpFc0/wJcFW/DlC8KgEJJmhvYHdiZmM+vsy+b2U+8Q9SRpP2BX3vnCP3yLnAL8CfgQjN71TlPmIIoAAoiaTpgc2A/YEfgQ66BQie8BQyK09z6RtL8pO1+P+ydJQzYO6RpgnOAa8xsvG+cMFEUAAWQtCyp0/8ssIhvmtAFfzWz7bxD1ImkC0kjYKFZhgPnAefE1sT+ogBwImkOYDdgf9L2u6HZ9jCzi7xD1IGkbYErvHOErrsT+A1wkZm94R2mjaIAqJikwaROf2dgVuc4oTr/Jm0T/Jp3kJJJmh14BFjUO0uozBjgz6Ri4AaLTqkyUQBUQNIspNPLvgwMco4T/PzGzA7wDlEyST8BvuidI7h5DPgxcJ6ZjfYO03RRAHSRpIWAQ4EhwLzOcUIZNjWzG71DlEjSusDtwHTeWYK714D/B5xpZs97h2mqKAC6QNLawOHArsTre+G9ngJWjm2C3ytvcHUvsJJ3llCUcaRXCc8wszu8wzRNVNodIml6SbtK+hvwd2AvovMP77cMcLx3iAJ9nej8w/vNQFosfbukuyTtmc+GCB0QIwADJGk24BDSvGVsyxt6Yxywlpk94B2kBJI+BjwAzOydJdTCi8DPSNMDcUrhAEQB0E95Yd8hpE8u8zvHCfVzN7Be27cJliTgJuDjzlFC/bwCnAT8LBYM9k9MAfSRpJkkHQo8DZxKdP6hf9YGvuQdogAHEZ1/6J95gR8Bz0g6XFLsnNpHMQLQS3mR0n7AN4l3lOvg36QFd08BT/b4907AsY65ehpF2iZ4mHcQD5IWJG33W8rhVt8jvY++TP5atse/P+qYK/TOi6Tf4a/MbKx3mDqIAmAaJE1Peof/W8BSznHCew1nyp38U1ObG8yF3H2Usx/DVWa2jXcID5IuIW2IVYKHgdWndpxt3rlzGaZcHCxYVcjQK8OA7wDnmtk47zAliwJgKvLc5B7ACcByvmlabQKpU38ofz1M7uzNbFR//oOS1gduo5wpsL3N7ALvEFWStCPp03YJJgAb9fc1s7wQeGJRMAhYOX8tQzn3WBs9DZwI/K7ta22mJgqAKZC0CvALYH3vLC0znEkd/cSvR81sTKcbkvQz0iZNJRhB2ib4Fe8gVZA0J2m734W9s2Rnmtlhnf6P5oXCKzCpIJj4FSMG1bobONjM7vUOUpooAHrI+5CfSFqcFe+ads9bwD+ZrLOvsgPMQ7qPUM7pi+ea2X7eIaog6eekN2hK8AKwYpWvk0mal/cXBSsBs1eVoYXGAz8HjjOzkd5hShEFQCZpZ9Ie1KV8KmmKcaTO/i7SBkl3kT7Vuw/JSdoB+It3jh42N7PrvUN0k6QNgVsBeWfJPmVml3mHkDQdabRgXWCd/H0l4oNIpw0HjjCzC72DlKD1BYCkpUibSmztnaUh/sV7O/t7uzGE3ymSLgZ28c6RPQOsVPL1GghJMwH3kzq6ElxiZrt6h5iaPIWwBu8tCpbwzNQg1wOHmtkT3kE8tbYAyA+jrwPHAPH+aP+MJJ3pPbHD/7uZ/cc3Ut9IWoD0Ktrc3lmyk8zs694hukHSCZSzDfLrpHUXL3sH6QtJ85OKgYkFwXrAnK6h6usd0j4CP2jr2RytLAAkbQKcRazu76u3SKvnb8xf95rZeN9IAyfpc8AvvXNk44B1zOw+7yCdJGlF0uuXM3lnyQ4ys7O9QwxUfk15DWBw/tqIWEvQV08Dh5jZdd5BqtaqAiD/sZwIHE28ntMbo0nHs07s8O9u4nu1+ZXPG4FPeGfJ7gHWbUJxBf+7vrcBG3hnyW4GBlsDH375oJy1mVQQbADM6hqqHgw4GTi2ic+4qWlNASBpEeACYGPvLAV7G7iD1BneBNzVlh21JC0HPEg5B9IcaWaneofoBElfAM70zpG9A6zSlrnfPNW5LrAJqSBYn5jy/CB3AHuY2XPeQarQigJA0rbAuaS9o8N7vQBcAVwODG3rXBiApGOB73rnyEaTFgQ+6x1kIHLh/Qgwh3eW7Dgz+553CC95v/xNge2B7SjnNdiSvArsX8LbId3W6AIgb/v6A+AIynntyJuRNsa4ArjczO53zlOMfL/cSznn0l9rZlt6hxgISX8BdvDOkf0TWGNq2/22kaTVmFQMrE08J3s6AziqyfdLYwsASUsAF5FWy7bdKOA60qf8v5rZv53zFEvSuqR1D6WsEfmMmf3WO0R/SNoV+IN3jmwCsIGZ3eUdpFSSPgpsSyoINgdm801UhLuB3es+Ejc1jSwA8qY+Z1POq10eXgUuIe23fqOZveOcpzYk/QT4oneO7L+k19X+6x2kLyTNTXq9cgHvLNlPzSyOX+4lSTOT1gzsRNon48O+iVy9ARxoZn/0DtJpjSsAJH2LtNK/jd4i7Wz3e9LwcWOHrropbwn9COUc+3y+mX3WO0RfSPol8DnvHNnzpO1+3/IOUkd5amwLYE/gU7T3NcPjzezb3iE6qVEFgKRTSfP9bTIWuIrrQV+hAAAZmElEQVTU6V9uZqOd8zSCpO1IUyal2NLMrvUO0Rt5n42hlDOfvL2ZXeEdogkkzUqaItiTtHtqKfs6VOU0M/uqd4hOaUQBkPfRPotyPnF023jSa3oXAH8ys9d94zSTpAuB3b1zZM+S3goousDLq8wfJB2NW4KLzGwP7xBNlKd5Pg3sRXrNcHrXQNU5GxhSwnkmA1X7AiAPT/0W2M07SwWGkW6+X5nZcO8wTZcXRT0KzOOdJTvVzI70DvFBJH2PtL12CV4jrZ+IRa9dJmlB4EDSh7DFneNU4Q/APnWfZq11AZAPy7gE2MY7SxeNB/5KGuG4uglVZ51IOgD4lXeObDxph8B7vINMiaRVgH8AM3pnyQ40s197h2iTPBq7FTCE9EZBk0cFrgR2qfPhXbUtAPJ57lcAH/fO0iUvkDqes83sBe8wbSZpKGlFdAnuI50VUNR2pfnBfwflvHZ7o5lt6h2izfImUJ8jjQw0dcOhW4DtzOxN7yD9UcsCQNK8wNXAWt5ZOsxIP9cvSO/rN2Iv+LqTtCxpXruULVSPMrOTvUP0JOnLpI1TSvA2abvfJ72DhP+dwbItcDBpdKCUxaGd8g9gKzN7xTtIX9WuAMiLjG4h7VrVFGNJ6xhONrPHvMOE95N0NPB97xzZGNKCwGe8gwBIWhx4mHI2jjnGzH7gHSK8n6Tlga8B+9CsNwjuBj5et63U61gAnAvU6p3oD/AmaW7/dDN7yTtMmLp8yto9wCreWbLrzWxz7xAAkq4kvRJWggeBNUubIgnvJWkh4CuktQKlnBMxUOeZ2b7eIfqiVgWApMOB071zdMC/gR8DPzezN7zDhN6RtDZwJ+VsE7yfmZ3rGUDSnqTXUUswAVjPzO72DhJ6R9JcwBeALwMfdY7TCV8xs1KmwqapNgWApE8C11DvVaXPAD8Czo2teetJ0unA4d45sldIr7mN8Gg8r8V5FJjPo/0pOMPMvuIdIvRd3np4X+DrwFLOcQZiPGnTrhu8g/RGLQoASUuR5ljquh/1COA7wC/q/t5o20majTTfXcq7zheY2d4eDUs6h/TQLsEwYJCZjfIOEvov7+tyMPBNyiks++pVYO1S1uh8kOILgPzAvQNY2TtLP4wGTgNOqutrIuH9JG1Nege4FFub2dVVNihpM9IJk6XYxsyu8g4ROiO/5n0UaWv3WZ3j9MdDwPqlF6RFFwCSBFwM7OydpY/Gk97hPyF27GsmSReQ9kMvQaWffvMGXP+knKHa35vZXt4hQuflHQZPIO0lULfp3z8Cu1rBnWwpi5mm5ijq1/lfRnpFa0h0/o12OGmorwSLk6aYqnIi5XT+r1LOmozQYWY23MyGACuRnq11sjOpDytWsSMAkhYGnqA+wz8vAYea2aXeQUI1JO0H/MY7RzaeNOTY1RXwklYnrccp5dPY/mZ2jneIUA1JOwJnAgt5Z+ml0cByZvaid5ApKXkE4LvUo/M34P9Iq7Gj82+R3PGUstp3euCXeb+Crsg7up1NOZ3/DdH5t0t+xq5AeuaW+en1vWYl9WVFKnIEQNJqpE1XSi5QIL0CdZCZ/c07SPAhaWnSgp9ZvLNkR5vZD7vxH5Z0JFDKFsRjgJXN7GnvIMGHpA2BX5IKgpJNIG1Odb93kMmV2sGeSrnZAMaR5kFXi86/3XIHdKJ3jh6Ol7RMp/+j+VXckn7OE6Pzb7f87F2NdF+WvPPjdKQ+rTjFjQBI2pZ0yl+pngf2MLPbvYOEMuRh97tJD6MSDDWzT3byPyjpWqCIrYf5/+3debRdZXnH8e8DCSIJoxAQEBnFMIkopESxVFhWJgMErdjWiiNUFzgBpQ7oQkQxRYSKxQqCgSWihiANVGSoikAYhJIAyhjAKiFhTiCQG57+8b7n3nNvbnKnc87z7rN/n7X2Oucm4e7fPST7efa7935fuJP0nHXJB33pIDObClwCvC46y2oc7O5zokM0K+osOx9ISxliHMwVpLN+FX/plQvRx0g34pXgnWZ2VKu+mZl9kHKK/wrSZTcVf+mVj8m7k47RpfpWO+/RGY2iGgDSQbTE6znLgc8D09y9lEe/pCDufhtpfYdSzDCzSWP9Jma2CWkyq1J8J3/WIv3kY/M00rG6xBlXJ5NqXDGKuQRgZhOBB4ExH7Ra7E/AEe4+NzqIlC3PWjkf2Do4SsMl7j6myYrM7GKglEl2FpDm2Ch6djWJZ2ZTgJ8BW0ZnGeAJYDt3XxIdBMoaATiU8or/H4CpKv4yHLkwHR2do8n78z01o2Jm76ac4g9wtIq/DEc+Zk8lHcNLMolU64pQUgNwRHSAAW4D9nH3x6KDSHW4+y+Bi6NzNDknj66NSB7N+I825Bmti/NnKzIs+di9D+lYXpJial0RlwDyAWoRsHZ0luxa4NBShmmkWvJ183uB10Rnyc5y9+NG8h9o2WPpFrm+zAZa+mTMGCwDNimhvpQyAnAQ5RT/2aSVxcL/50g15UL12egcTT6Vr4kOi5ntCRzbxjwj9VkVfxmtfCw/kHRsL8HapJoXrpQGoJQhkd8BR7r7y9FBpNrc/UeUs1zuGqRpgscP9QfzY0o/oJxjw6/yZykyavmYfiTpGF+CImpe+D9yM1uH1J1Fu5/0mN+y6CDSNY4mLQZSgl2B44fx544HdmtzluF6gbJuqpQKy8f2aaRjfbQDc+0LFd4AAAcQv+jPYtKw/5PBOaSLuPtDwMnROZp8yczesKrfNLMdgC93MM9QTs6foUhL5GP8gaRjfqR1SLUvVAkNwPTg/b8CHObuDwTnkO70beD30SGytYFzzcxW8fvfp5x7cX5P+uxEWiof6w8jHfsjRde+2AYgLy96cGQG4Gx3vyE4g3Qpd19BWdME7wt8ZOAvmtlH8u+VoDHdbymfmXSZfMw/OzjGwbkGhgl9DDAPR/4xLAA8CuysO/6l3czsW6QpSkvwDOmxuscBzGxT0mOLG4am6jPD3Ydzv4LIqOXHA+8GtgqMsaO73xe18+hLADsF7/8YFX/pkJOBh6NDZBsAZzV9fTblFP+HKeu+CelS+dh/THCM0BoY3QBELvxznbtfGbh/qRF3fwH4RHSOJu81s0PM7BDgvdFhmnwif1YibZdrwHWBEUIXv4tuACK7n+8H7ltqyN1/BcyMztHknLyVYmb+jEQ6KbIWhI4ARN8D8Fvg7QG7XgRsqQl/pNPM7DWkBUo2js5SmMXAG/UornSama1FWvV1k4Dd3+Du+wTsF4gfAVgvaL8XqfhLhFzgSpljvySfVvGXCLkWXBS0+6gaCMQ3AOsG7be01aGkRtz9YkAr2/X5Zf5MRKJE1YSoGgjENwBR3Y8m/ZFoJU0THEnT/UoJomqCRgACqAGQUO6+APhSdI4CfCl/FiKRompCrUcAlgftd8hV0UQ64DvA7dEhAt1O+gxEokXVhLi78IlvAJ4I2u/uQfsV6ZWnuv0o0BOdJUAP8FFN9yuFiFoB85mg/QLxDcDCoP2qAZAiuPudwBnROQKckX92kRK8KWi/tW4ANAIgAl8BHowO0UEPkn5mkVJoBCBA1AjAm4P2K7ISd3+RsqYJbrdP5J9ZpBRRNaHWDUDUCMCOZrZv0L5FVuLu1wIXROfogAvyzypSBDPbB9glaPeLgvYLxDcAUSMAAF8P3LfIYD5H8AGhzRaRfkaRkpwWuO/5gfsObwAeC9z33mZ2cOD+Rfpx96eA46JztNFx+WcUKYKZHQS8LTBC6I2w0YsBbUQ6K4hqRO4CdvfID0FkADO7EjggOkeLXeXuB0aHEGkwMwPuIO4JAIDN3D1sJDx0BCCfDdwaGGE34MjA/YsM5hhgaXSIFlpK+plESvIBYov/45HFH+IvAQBcHbz/75rZG4MziPRy90eAL0bnaKEv5p9JpAhmtjNwTnCMO4L3X0QDEL0q2gbAHDPT+uxSkrOIHR1rlVtJP4tIEcxsEvBfBC/EQ/zJb+w9AABmNg54kvj/Gb8D9nP3l4JziABgZruR5ssfF51llHqAt7j7XdFBRADMbG3gf4ApwVEAtoleCCt8BMDde4DronOQ7gQ9PzqESEMunDOic4zBDBV/KUW+6e9Cyij+d0YXfyigAciiLwM0fMDMvhIdQqTJV6nm8tUPkLKLlOJU4H3RIbLLogNAOQ3AVcAr0SGyk83stNwtioRy92XAx6NzjMLHc3aRUGa2hpmdCZwUnaWJGoCGfIfwT6JzNPkX4FIze3V0EBF3v55qXZ46P2cWCWVmE4DZlDXB1i3uPi86BBRwE2BDfixjHlDSmfdcYFr0s5oiZrYhcC+waXSWISwEJrv709FBpN7MbHPgCmCP6CwDvM/dfxodAgoZAQBw97uBWdE5BpgCzM3NiUiYXFBLOotZleNU/CVafoJmLuUV/4coqM4V0wBkX4sOMIjXAzea2buig0i9uftPgDnROVZjTs4oEsbMDgBuALaMzjKIM9x9RXSIhmIuATSY2S+AQ6JzDGIF8E3gq+7+cnQYqSczex1wDzAxOssAS4Cd3D1ygS+psfyM/9eAz1DeyS2k+W62cvcXooM0lPghnRIdYBXWBP4VuN3M3hodRuopF9gvROcYxBdU/CWKmU0hTa37OcqsawCnlFT8ocARAAAzuwp4d3SO1egBTkejARLAzNYAbqSMCU0gXWud6u6lPMorNWFmryLNN/F50klaqe4mrTzbEx2kWakNwFTS1Lylmw8c5e63RQeRejGzXUnTBI8PjrKcNN1vEY81SX3kkdgLgCrcpP3OEh+NLXKoxN1vBH4cnWMYdgFuMrNTzWyt6DBSH7ngnh6dAzhdxV86yczWMrNTgJuoRvG/tMTiD4WOAACY2UakM+zXRmcZpj8CJ7r75dFBpB7yTU//C7whKMJ9wJs04590ipkdBnyDuL/zI7WUNC9GkffHFDkCAODuTwEfi84xAjsCs83sN/mGFJG2apomOKKLdzTdr3SImU01s9+RnqGvSvEH+FSpxR8KbgAA3H0O1ZoCFWAf4GYzu9TMtosOI93N3X8NnBew6/PyvkXaxszeYGazSPeETY3OM0IXufsF0SFWp9hLAA1mth5wG7BDdJZRWA58j/T4x+LoMNKdzGwD0jTBm3Vol4+ThjWf6dD+pGbMbFPgZNIo8LjgOKNxP7CHuy+JDrI6RY8AALj7c8B7gOeis4zCeOBY4EEzO0mLC0k75EJ8bAd3eayKv7SDmU0wsy+TlpM+hmoW/5eAvyu9+EMFRgAazOxA0sIOxTctq/Fn4CzgXB1ApdXM7OfA4W3ezSx3n97mfUjNmNnGwCeBTwEbB8cZq6Pd/dzoEMNRmQYAwMyOp4xHn8ZqCem67ZnuviA4i3QJM5tIula6W5t2cRfwtiqc2Ug1mNm2wGeBo4B1guO0wjfc/aToEMNVqQYAwMwuBD4YnaNFVgA/B2a4+63RYaT6zGwr4FZgUou/9RPAnu7+aIu/r9RQnsTnBNKIVckz+I3ETOCfvEJFtYoNwHjgZ6T7ArrJb4EZwBVV+gsk5TGzvYDLad1NgY8D09z9lhZ9P6mpvFLfCcC+wVFa7RrgQHdfHh1kJCrXAEDv/M+XA38bnaUN7gPOAH7k7i9Gh5FqMrNJwIWMfU2N/yad1Twx9lRSR/l4/X7SfP27BMdphzuBd7j789FBRqqSDQBAvqP+Srqvk2x4FrgEOF9nXjIaZmbAp4GTgE1G+J8vAk4j3adSzYOEhDKzPUjX9j8AbBQcp11+D7zL3Z+MDjIalW0AoPemp19SvQkiRupu4IfATJ2JyUjldSoOJT1TvR9gq/ijDlwL/CcwWytdykjlu/n/gVT423UzailuAg5w92ejg4xWpRsA6J0oaDbwN9FZOqAHmENqBuaUtrSklM/M1ge2AbbOG8CCvD1c5YOZxDCzcaRLTUcBhxC/QmUnXA+8p+pPxFS+AYDeM5wfkoaa6mIhcBHpEsE90WFEpF7MbDKp6P8jnZuFsgRXAYd3wzoYXdEAQO/1ztOAE6OzBLiF9AjKZe7+f9FhRKQ7mdnrgMNIJ1t1XPTsXNJMmF1xeaxrGoAGM/tn4GyqPWPgaDmpGZhFagbuD84jIhVnZjuQntefDuwZHCfKC6QZ/mZGB2mlrmsAAMxsGml4fGJ0lmDzgctI07feGR1GRKrBzHajr+h346N7I3E/MN3d50UHabWubAAAzGxH0oRBdf/L2/AwuRkAbnL3V4LziEgh8iXUvUhF/3Bg+9hExfg58OG8KF3X6doGAMDM1gG+C3woOEppFpKenLgM+HU33MwiIiOTJ+h5G+kR0cOALWMTFaUHONHdz4gO0k5d3QA0mNlRpEZAy/GubBlwI2kqy2uA2zU6INJ9zGwNYHdg/7y9HR0TB/Nn0nK+N0QHabdaNAAAZrYr8FNgx+gshXua9IzrtcA17n5fcB4RGSUz245U7PcD3gm8JjZR8a4HjnT3hdFBOqE2DQCAmU0AvkFad3pVs6FJf4/RNzpwnbs/HpxHRFbBzDYhFfrGWf7WoYGqw4FvAl909xXRYTqlVg1Ag5ntA5wH7BCdpYLmk5sB4GZ3XxScR6S2csGfQloTZX/S9Ls6uRmZB4BPuvvV0UE6rZYNAPQuJnQK8BnqOWdAqzwIzAVuztudVVsSU6QK8lLouwN/1bRtGxqq2l4kTR53uru/FB0mQm0bgAYzmwKcD+wUnaVLLAPuoK8huNndH42NJFI9eda95mK/B7B2aKjucTnwaXdfEB0kUu0bAOh9HOYk4AR0V2w7/IX+owS3ufvS2Egi5ciPLL+VvmI/Bdg8NFR3epA0le+V0UFKoAagSe64vwkcGZ2ly60gLXF8FzCPdF/BPHd/LDSVSAeY2VbArgO2ycC4yFxdrvbD/YNRAzAIM9sb+Db1XOwi0rOkZmA+/RuDp0JTiYyCmW1Imom0udDvAqwfmauGfgEcV/fh/sGoAViFPDXm35O6Rs2QFesvNDUE+fUed38hNJUIvZcQJ7PyWf0WkblEw/1DUQMwhHxt7gTgc2hxoZK8AjxEWqjjobw93Hjv7s8HZpMuk48D2wDbke68b2zb523NuHQywLPAv6Hh/iGpARgmM9sY+DxpEiE1AuVbzCCNQd4eq9NkHzK0POL3WvoX923pK/ibxaWTYVoMnAn8u7s/Gx2mCtQAjJAaga7QAzxC/+bgEeDxxubuz8TFk1bLs4BuBmyaX7ek/9n8NugJoKr6MzADOFeXBUdGDcAoqRHoestoaggG2f6SXxdqmDFGvvbeKOibDfFe/0a7z8Okp7Yu0L/B0VEDMEZqBIS0gNLABuFp4LkhtiVe83+AeYW6dUl3xq+Xt+b3ja/Xp6+oN143CIgs8e4l3Zz9Y3fviQ5TZWoAWiQ/8vMxUiOwVXAcqQYHnqd/UzDw695mAXgZWJ63nqb3Y/k1gPGkZ9DHD9gG/tpw/kxjm8DghXzg+wlo7noZnjuArwOztGR5a6gBaDEzWxM4DDiOtN62iIiM3o3AqXqcr/XUALSRme1BagTeD6wVHEdEpCpeAi4Dvufuv4kO063UAHSAmW0KHAMcTbp+KSIiK5tHWqp9pmYAbT81AB1kZmuRLg98mLR2t5YhFpG6ex64BDjP3edGh6kTNQBB8sJDH8qb1vQWkbq5CfgB8BOtDhpDDUCwPAPZvqRRgeloMhIR6V6LgZnAD9z9nugwdacGoCBmth5pKeIPA3sFxxERaQUHriGd7c9295eD80imBqBQZjYZOII0KvCm4DgiIiN1KzALuERL8ZZJDUAFmNn2pEZgOrBncBwRkcGsAG4gFf3L3P2x4DwyBDUAFWNmWwGHk0YH9kZPEohInJdJw/uzgF+4+6LgPDICagAqzMxeS3qscDrw12hNchFpv6XAlaSJeua4+3PBeWSU1AB0ibwo0TTSyMB+pPnYRURa4SngCtKZ/tXuviw4j7SAGoAuZGYbAAcB7yJNOLR5bCIRqaD7gatJZ/q/1sp73UcNQA3kJwr2z9u+pFXYRESa/Qm4DrgWuM7d/xScR9pMDUDNmNk40pMEjYZgb3S5QKSOFgPXk4u+u98fnEc6TA1AzZnZBOAd9DUEu6L12UW60fPAb8hn+MBdrgJQa2oApB8zm0S6iXD//Pr62EQiMkrLgBvpG9a/TdfxpZkaAFktM9scmNK0vRWYGBpKRAbzKHALaQa+ucBc3a0vq6MGQEbEzNYAdqavIdgrf605CEQ65ylSob+VVPRvcfeFsZGkatQAyJiZ2UTgLfQfKdgiNJRI93gRuIP+xf6B2EjSDdQASFuY2Rb0HyV4M7B+aCiR8q0A7qFvKP8WYJ6u3Us7qAGQjjGzLUmXC3Zpet0JmBCZSySAk67Z35O3u/PrfHdfGhlM6kMNgIQyMwO2pn9TsDMwGXhVXDKRlngFWEBfoW8U+3tV6CWaGgApkpmtCWxHagiam4Md0MRFUp4VwEOsXOj/4O4vRgYTWRU1AFIpZjYe2BbYZhXbRnHppMu9ADxCOqNv3v5IKvQvBeUSGRU1ANJVzGw9Vt0cbAOsE5dOCreUwQv8AuARd38iJpZIe6gBkFrJMx0ObAq2ADbN2yRgrbCA0i49pLnvF5IWvVkwcHP3xTHRRGKoARAZwMw2pK8hGGpbOyimpOfjF+btiVW8Nt4/qXnvRfpTAyAyBvmSw8CmYBPSnAfrAevm18HejwuIXBoHlpAWqnmuaWv+ehErF/SF7r4kIrBIt1ADIBLEzF7N0E1C4/1E0qWJcaSnIEbyurrfgzQ83gMsb8H7l1l9MR/4a0vc/ZWxfZIiMhr/D/mVnAvyCSBDAAAAAElFTkSuQmCC");
  width:                            1.1rem;
  height:                           1.0rem;
} 


/* Permanent Notes */
span[data-link-title="Permanent Notes"] .rm-page-ref {
  color: #f5f5f5 !important;
}

span[data-link-title="Permanent Notes"] .rm-page-ref__brackets {
  display: none;
}
span[data-link-title="Permanent Notes"] {
  background-image: linear-gradient(90deg, #6bcc77, #6bcc77);
  background-size: 100%;
  color: #2d303c !important;
  padding: 2px 5px 2px 8px;
  font-size: 13px;
  line-height: 1em;
  font-weight: 500;
  border-radius: 3px 0 0 3px;
  position:relative;
  margin-right: 0.5em;
  margin: 0 0.7em 0 0.1em
}

span[data-link-title="Permanent Notes"]:hover {
  background-image: linear-gradient(90deg, var(#79ff8a), var(#79ff8a));
}

span[data-link-title="Permanent Notes"] + span[data-link-title] { 
  background: #2d303c;
  color: #f5f5f5;
  padding: 3px 5px 3px 15px;
  font-size: 13px;
  line-height: 0.9em;
  font-weight: 400;
  border-radius: 0 3px 3px 0;
  margin-left: -10px;
}

span[data-link-title="Permanent Notes"]:after,
span[data-link-title="Permanent Notes"]:before {
  left: 100%;
  top: 50%;
  border: solid transparent;
  content: " ";
  height: 0;
  width: 0;
  position: absolute;
  pointer-events: none;
}

span[data-link-title="Permanent Notes"]::after {
  color: #f5f5f5;
  border-left-color: #6bcc77;
  border-width: 11px;
  margin-top: -11px;
}```
- 彩虹条
    - ```css
.rm-level-1 > .rm-multibar, .rm-level-19 > .rm-multibar, .rm-level-37 > .rm-multibar, .rm-inline-references > .rm-multibar {
    border-right-color: var(--indent1) !important;
    box-shadow: var(--box-shadow-values) var(--indent1) inset;
}

/* Level 2 */
.rm-level-2 > .rm-multibar, .rm-level-20 > .rm-multibar, .rm-level-38 > .rm-multibar {
    border-right-color: var(--indent2) !important;
    box-shadow: var(--box-shadow-values) var(--indent2) inset;
}

/* Level 3 */
.rm-level-3 > .rm-multibar, .rm-level-21 > .rm-multibar, .rm-level-39 > .rm-multibar {
    border-right-color: var(--indent3) !important;
    box-shadow: var(--box-shadow-values) var(--indent3) inset;
}

/* Level 4 */
.rm-level-4 > .rm-multibar, .rm-level-22 > .rm-multibar, .rm-level-40 > .rm-multibar {
    border-right-color: var(--indent4) !important;
    box-shadow: var(--box-shadow-values) var(--indent4) inset;
}

/* Level 5 */
.rm-level-5 > .rm-multibar, .rm-level-23 > .rm-multibar, .rm-level-41 > .rm-multibar {
    border-right-color: var(--indent5) !important;
    box-shadow: var(--box-shadow-values) var(--indent5) inset;
}

/* Level 6 */
.rm-level-6 > .rm-multibar, .rm-level-24 > .rm-multibar, .rm-level-42 > .rm-multibar {
    border-right-color: var(--indent6) !important;
    box-shadow: var(--box-shadow-values) var(--indent6) inset;
}

/* Level 7 */
.rm-level-7 > .rm-multibar, .rm-level-25 > .rm-multibar, .rm-level-43 > .rm-multibar {
    border-right-color: var(--indent7) !important;
    box-shadow: var(--box-shadow-values) var(--indent7) inset;
}

/* Level 8 */
.rm-level-8 > .rm-multibar, .rm-level-26 > .rm-multibar, .rm-level-44 > .rm-multibar {
    border-right-color: var(--indent8) !important;
    box-shadow: var(--box-shadow-values) var(--indent8) inset;
}

/* Level 9 */
.rm-level-9 > .rm-multibar, .rm-level-27 > .rm-multibar, .rm-level-45 > .rm-multibar {
    border-right-color: var(--indent9) !important;
    box-shadow: var(--box-shadow-values) var(--indent9) inset;
}

/* Level 10 */
.rm-level-10 > .rm-multibar, .rm-level-28 > .rm-multibar, .rm-level-46 > .rm-multibar {
    border-right-color: var(--indent10) !important;
    box-shadow: var(--box-shadow-values) var(--indent10) inset;
}

/* Level 11 */
.rm-level-11 > .rm-multibar, .rm-level-29 > .rm-multibar, .rm-level-47 > .rm-multibar {
    border-right-color: var(--indent11) !important;
    box-shadow: var(--box-shadow-values) var(--indent11) inset;
}

/* Level 12 */
.rm-level-12 > .rm-multibar, .rm-level-30 > .rm-multibar, .rm-level-48 > .rm-multibar {
    border-right-color: var(--indent12) !important;
    box-shadow: var(--box-shadow-values) var(--indent12) inset;
}

/* Level 13 */
.rm-level-13 > .rm-multibar, .rm-level-31 > .rm-multibar, .rm-level-49 > .rm-multibar {
    border-right-color: var(--indent13) !important;
    box-shadow: var(--box-shadow-values) var(--indent13) inset;
}

/* Level 14 */
.rm-level-14 > .rm-multibar, .rm-level-32 > .rm-multibar, .rm-level-50 > .rm-multibar {
    border-right-color: var(--indent14) !important;
    box-shadow: var(--box-shadow-values) var(--indent14) inset;
}

/* Level 15 */
.rm-level-15 > .rm-multibar, .rm-level-33 > .rm-multibar, .rm-level-51 > .rm-multibar {
    border-right-color: var(--indent15) !important;
    box-shadow: var(--box-shadow-values) var(--indent15) inset;
}

/* Level 16 */
.rm-level-16 > .rm-multibar, .rm-level-34 > .rm-multibar, .rm-level-52 > .rm-multibar {
    border-right-color: var(--indent16) !important;
    box-shadow: var(--box-shadow-values) var(--indent16) inset;
}

/* Level 17 */
.rm-level-17 > .rm-multibar, .rm-level-35 > .rm-multibar, .rm-level-53 > .rm-multibar {
    border-right-color: var(--indent17) !important;
    box-shadow: var(--box-shadow-values) var(--indent17) inset;
}

/* Level 18 */
.rm-level-18 > .rm-multibar, .rm-level-36 > .rm-multibar, .rm-level-54 > .rm-multibar {
    border-right-color: var(--indent18) !important;
    box-shadow: var(--box-shadow-values) var(--indent18) inset;
}

/* Focused block */
.rm-focused > .rm-block-children > .rm-multibar {
  border-right: dotted;
  box-shadow: none;
}


:root {
    --box-shadow-values: 25px 0px 20px -30px; 
      
    --indent1: #EA0A16F2;
    --indent2: #F206EF;
    --indent3: #FF9800;
    --indent4: #009688;
    --indent5: #3AFF22;
    --indent6: #FFEB3B;
    --indent7: #A808E8AD;
    --indent8: #303472AD;
    --indent9: #395C45AD;
    --indent10: #7C7948AD;
    --indent11: #7D5039AD;
    --indent12: #A5494FAD;
    --indent13: #706597AD;
    --indent14: #657D91AD;
    --indent15: #6D8D76AD;
    --indent16: #A09A84AD;
    --indent17: #987174AD;
    --indent18: #8B5F78AD;
}

.rm-multibar {
  z-index:4;
}```
- Element Class Detail 发现没有关联的概念
    - ```css
.rm-level3, .rm-heading-level-3>.rm-block__self .rm-block__input
{ color: #0C403B;
 font-weight:600;
} ```
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
- 对一个block设置字体颜色和背景颜色
    - ```css
/* 模拟马克笔效果的样式 */
.roam-block-container[data-page-links*="zise"] > div.rm-block-main {
  background: linear-gradient(135deg, rgba(211, 92, 232, 0.3), rgba(211, 92, 232, 0.15));
  padding: 2px 4px;
  border-radius: 5px;
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
}

.roam-block-container[data-page-links*="lanse"] > div.rm-block-main {
  background: linear-gradient(135deg, rgba(102, 176, 245, 0.3), rgba(102, 176, 245, 0.15));
  padding: 2px 4px;
  border-radius: 5px;
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
}
span[data-link-title="lanse"] { 
    display: none !important; 
}
.roam-block-container[data-page-links*="hongse"] > div.rm-block-main {
  background: linear-gradient(135deg, rgba(234,35,35,0.3), rgba(241,225,225,0.15));
  padding: 2px 4px;
  border-radius: 5px;
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
}
span[data-link-title="hongse"] { 
    display: none !important; 
}

.roam-block-container[data-page-links*="lvse"] > div.rm-block-main {
  background: linear-gradient(135deg, rgba(208, 243, 173, 0.3), rgba(208, 243, 173, 0.15));
  padding: 2px 4px;
  border-radius: 5px;
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
}
span[data-link-title="lvse"] { 
    display: none !important; 
}
.roam-block-container[data-page-links*="huangse"] > div.rm-block-main {
  background: linear-gradient(135deg, rgba(237, 241, 194, 0.3), rgba(237, 241, 194, 0.15));
  padding: 2px 4px;
  border-radius: 5px;
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
}
span[data-link-title="hse"] { 
    display: none !important; 
}```
    - ```plain text

/*To style an entire block, and all its child elements, we use:*/
/*.roam-block-container[data-page-links*="zise"] {
  background: #D35CE8;
}*/

/*To style only the child elements but not the parent, add .rm-block-children to the end use:*/

.roam-block-container[data-page-links*="lanse"] .rm-block-children {
  background: #66B0F5;
}

/*To style just the block itself but none of the child elements, add */
.roam-block-container[data-page-links*="hongse"] > div.rm-block-main {
  background:rgba(241,194,194,0.93);
}
span[data-link-title="hongse"] { 
    display: none !important; 
}
.roam-block-container[data-page-links*="lvse"] > div.rm-block-main {
  background:rgba(208,243,173,0.93);
}
span[data-link-title="lvse"] { 
    display: none !important; 
}
.roam-block-container[data-page-links*="huangse"] > div.rm-block-main {
  background:rgba(237,241,194,0.93);
}
span[data-link-title="huangse"] { 
    display: none !important; 
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
- ^^tag^^
    - ```html
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
- pdf优化
    - ```clojure
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
- 极简模式
    - {{roam/css}}
        - ```plain text
/* Bullet Zoom Focus v2.6 by Jeff Harris
  When zoomed in on a bullet add the tag #.rm-focus to the parent block to create a minimal writing environment. 
  This only works when zoomed in so there is no need to remove the tag when done.
*/
@import url('https://jmharris903.github.io/Railscast-for-Roam-Research-Theme/fonts/calendas-plus.css');

.zoom-path-view + div .rm-focus div,
.zoom-path-view + div .rm-focus textarea {
  font-family: 'Calendas Plus', 'Lora', 'Droid Serif', 'Georgia', serif !important;
  font-size: 1.43rem;
  /* space between lines */
  line-height: 1.5em;
}

.zoom-path-view + div .rm-focus.rm-heading-level-1 > .rm-block__self .rm-block__input,
.zoom-path-view + div .rm-focus .rm-heading-level-1 > .rm-block__self .rm-block__input,
.zoom-path-view + div .rm-focus.rm-heading-level-2 > .rm-block__self .rm-block__input,
.zoom-path-view + div .rm-focus .rm-heading-level-2 > .rm-block__self .rm-block__input,
.zoom-path-view + div .rm-focus.rm-heading-level-3 > .rm-block__self .rm-block__input,
.zoom-path-view + div .rm-focus .rm-heading-level-3 > .rm-block__self .rm-block__input,
.zoom-path-view + div .rm-focus .rm-heading-level-1,
.zoom-path-view + div .rm-focus .rm-heading-level-2,
.zoom-path-view + div .rm-focus .rm-heading-level-3 {
  font-family: 'Calendas Plus', 'Lora', 'Droid Serif', 'Georgia', serif !important;
}

.zoom-path-view + div .rm-focus .rm-multibar {
  display: none;
}

.zoom-path-view + div .rm-focus .rm-bq {
  font-size: 18px;
}

.zoom-path-view + div .rm-focus .rm-hide-bullet > .rm-embed-inner-block-hide {
  margin-left: -30px;
}

.zoom-path-view + div .rm-focus .rm-embed-show-bullet .rm-embed-inner-block-hide {
  margin-left: -2px;
}

.zoom-path-view + div .rm-focus.roam-block-container .roam-block-container {
  /* space between blocks */
  margin-top: 0.7em;
}

.zoom-path-view + div .rm-focus .rm-block__controls {
  visibility: hidden;
}

.zoom-path-view + div .rm-focus .rm-block__self:hover .rm-block__controls {
  visibility: visible;
}```
- [[Tag Styles]][[lvse]]
    - ```python
span.rm-page-ref[data-tag="笔记"],
span[data-link-title^="软件联动"] .rm-page-ref {
  color: #fcb815;
  padding: 3px 4px;
  font-weight: 700;
  line-height: 1.4em;
}```
    - {{[[roam/css]]}}
        - ```css

/* Custom data tags */
span.rm-page-ref[data-tag="memo"]:before {
    content: '📝'}
span.rm-page-ref[data-tag="memo"] {
    background: #9769FF8E !important;
    color: white !important;
    padding: 3px 7px;
    font-weight: 500;
    line-height: 2em;
}
span.rm-page-ref[data-tag="参考资料"] {
    background: #9769FF8E !important;
    color: white !important;
    padding: 3px 7px;
    font-weight: 500;
    line-height: 2em;
}
span.rm-page-ref[data-tag="读书笔记"]:before {
    content: '📖'
}
span.rm-page-ref[data-tag="读书笔记"] {
    background: rgba(255,170,214,0.68) !important;
    color: white !important;
    padding: 3px 7px;
    font-weight: 500;
    line-height: 2em;
}
span.rm-page-ref[data-tag="srs/cloze"] {
    background: rgba(255,170,214,0.68) !important;
    color: white !important;
    padding: 3px 7px;
    font-weight: 0;
    line-height: 2em;
}
span.rm-page-ref[data-tag="低效"] {
    background: #B8B2B2 !important;
    color: white !important;
    padding: 3px 7px;
    font-weight: 500;
    line-height: 2em;
}
span.rm-page-ref[data-tag="睡眠"] {
    background: #B8B2B2!important;
    color: white !important;
    padding: 3px 7px;
    font-weight: 500;
    line-height: 2em;
}
span.rm-page-ref[data-tag="阅读"] {
    background: rgba(255,170,214,0.48) !important;
    color: white !important;
    padding: 3px 7px;
    font-weight: 500;
    line-height: 2em;
}
span.rm-page-ref[data-tag="财富"] {
    background: #2590E4!important;
    color: white !important;
    padding: 3px 7px;
    font-weight: 500;
    line-height: 2em;
}
span.rm-page-ref[data-tag="爱好"] {
    background: #06BE0D7C!important;
    color: white !important;
    padding: 3px 7px;
    font-weight: 500;
    line-height: 2em;
}
span.rm-page-ref[data-tag="技能"] {
    background: rgb(255,170,214) !important;
    color: white !important;
    padding: 3px 7px;
    font-weight: 500;
    line-height: 2em;
}
span.rm-page-ref[data-tag="育儿"]:before {
    content: '👨‍🍼'
}
span.rm-page-ref[data-tag="育儿"] {
    background: #E341FF6B !important;
    color: #1A1918 !important;
    padding: 3px 8px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="健康"] {
    background: #2590E475!important;
    color: #2B2D2D !important;
    padding: 3px 3px;
    font-weight: 600;
    line-height: 1.4em;
}

span.rm-page-ref[data-tag="家庭"] {
  background: #E341FF7F !important;
    color: #201E20 !important;
    padding: 3px 4px;
    font-weight: 700;
    line-height: 1.4em;
}

span.rm-page-ref[data-tag="洞见"]:before {
    content: '🦩'
}


span.rm-page-ref[data-tag="Garden Notes"] {
    color: #9DBC1300;
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
    background: #ADCB2A72;
    color: #fff;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}
span.rm-page-ref[data-tag="工作"] {
    background: #FF980070;
    color: #3D3939;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="标准化"] {
    color: #8C41A677;
    padding: 3px 4px;
    line-height: 1.4em;
    font-weight: 700;
}



span.rm-page-ref[data-tag="Researching"] {
    background: #FF9D66 !important;
    color: #fff;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}



span.rm-page-ref[data-tag="写作"] {
    background: rgba(255,170,214,0.41) !important;
    color: #fff !important;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}
span.rm-page-ref[data-tag="人际"] {
    background:rgba(255,170,214,0.45) !important;
    color: #fff !important;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}```
- 数字花园[[hongse]] @评论:暂时暂停使用，因为和roam-tookit里面的功能冲突
    - ```html


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

/* div[style*="width: 580px;"], div[style*="width: 720px;"] {
    width: 100% !important;
    max-width: 1100px !important;
}

div[style*="height: 720px;"] {
    height: 85vh !important;
}

Search bar wide when typing in it 


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
*/

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
    - ```html

div[style*="padding-right: calc((100% - 800px) / 2); padding-left: calc((100% - 800px) / 2);"], div[style*="padding-right: calc((100% - 568px) / 2); padding-left: calc((100% - 1032px) / 2);"] {
    
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

/* Search bar wide when typing in it 

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
*/
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
