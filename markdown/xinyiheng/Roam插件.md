- chrome插件商店中的插件
    - [[roam portal]]可以展示概念之间的立体图，非常棒，我设置了
#[[快捷方式]]ctrl+p
    - [[Roam Highlighter]]
    - [[roam toolkit]]很早就安装了，但是很少使用，最近知道了它可以把卡片以思维导图的方式展示出来，感觉很惊艳，可以使用。我设置了调出这个插件的#[[快捷方式]]ctrl+i
        - ```javascript
```
- [[roam extentions]]基本上都是以[[roam/js]]为开头的
    - ExtensionsVia[RoamJS Extensions](https://roamjs.com/extensions) [[20220117]] 上午10:21 @评论:这是最全的一个寻找roam插件的地方。它还推出了一个叫做、的插件专门管理下载的插件，可以说层层嵌套了。
    - [[roam42]]的最特别，它最早提出了SmartBlock的概念，后来被官方接纳，不过两者差别还不小。smartblock有些自带的功能非常隐蔽，比如我探索的block mention lists这个功能就很隐蔽。
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
    - sidebar
    - mindmap
        - {{[[roam/js]]}}
            -   ```javascript
var existing = document.getElementById("roamjs-mindmap");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/mindmap.js";
  extension.id = "roamjs-mindmap";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}
```
  ```
- 还有一些独立开发者基于[[roam/js]]开发的插件
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
    - 在roam research中实现类似anki的间隔记忆
        - [[roam/sr]]
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
    - telegroam  @评论:从telegram中直接发信息同步到roam research
        - {{[[roam/js]]}}
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
    - bullet path@评论:显示当前block的路径
        - {{[[roam/js]]}}
            - ```javascript
// BULLET
let scale = 2;
let bulletColor = '#07FA11';

// LINES
let showLines = true;
let lineWidth = 2;
let lineColor = bulletColor;
let borderRadius = 5;

// HIGHLIGHT REFS
let highlightRefs = true;
let refColor = bulletColor;

/* ======= LIBRARIES ======== */

/*
 * arrive.js
 * v2.4.1
 * https://github.com/uzairfarooq/arrive
 * MIT licensed
 *
 * Copyright (c) 2014-2017 Uzair Farooq
 */

var Arrive=function(e,t,n){"use strict";function r(e,t,n){l.addMethod(t,n,e.unbindEvent),l.addMethod(t,n,e.unbindEventWithSelectorOrCallback),l.addMethod(t,n,e.unbindEventWithSelectorAndCallback)}function i(e){e.arrive=f.bindEvent,r(f,e,"unbindArrive"),e.leave=d.bindEvent,r(d,e,"unbindLeave")}if(e.MutationObserver&&"undefined"!=typeof HTMLElement){var o=0,l=function(){var t=HTMLElement.prototype.matches||HTMLElement.prototype.webkitMatchesSelector||HTMLElement.prototype.mozMatchesSelector||HTMLElement.prototype.msMatchesSelector;return{matchesSelector:function(e,n){return e instanceof HTMLElement&&t.call(e,n)},addMethod:function(e,t,r){var i=e[t];e[t]=function(){return r.length==arguments.length?r.apply(this,arguments):"function"==typeof i?i.apply(this,arguments):n}},callCallbacks:function(e,t){t&&t.options.onceOnly&&1==t.firedElems.length&&(e=[e[0]]);for(var n,r=0;n=e[r];r++)n&&n.callback&&n.callback.call(n.elem,n.elem);t&&t.options.onceOnly&&1==t.firedElems.length&&t.me.unbindEventWithSelectorAndCallback.call(t.target,t.selector,t.callback)},checkChildNodesRecursively:function(e,t,n,r){for(var i,o=0;i=e[o];o++)n(i,t,r)&&r.push({callback:t.callback,elem:i}),i.childNodes.length>0&&l.checkChildNodesRecursively(i.childNodes,t,n,r)},mergeArrays:function(e,t){var n,r={};for(n in e)e.hasOwnProperty(n)&&(r[n]=e[n]);for(n in t)t.hasOwnProperty(n)&&(r[n]=t[n]);return r},toElementsArray:function(t){return n===t||"number"==typeof t.length&&t!==e||(t=[t]),t}}}(),c=function(){var e=function(){this._eventsBucket=[],this._beforeAdding=null,this._beforeRemoving=null};return e.prototype.addEvent=function(e,t,n,r){var i={target:e,selector:t,options:n,callback:r,firedElems:[]};return this._beforeAdding&&this._beforeAdding(i),this._eventsBucket.push(i),i},e.prototype.removeEvent=function(e){for(var t,n=this._eventsBucket.length-1;t=this._eventsBucket[n];n--)if(e(t)){this._beforeRemoving&&this._beforeRemoving(t);var r=this._eventsBucket.splice(n,1);r&&r.length&&(r[0].callback=null)}},e.prototype.beforeAdding=function(e){this._beforeAdding=e},e.prototype.beforeRemoving=function(e){this._beforeRemoving=e},e}(),a=function(t,r){var i=new c,o=this,a={fireOnAttributesModification:!1};return i.beforeAdding(function(n){var i,l=n.target;(l===e.document||l===e)&&(l=document.getElementsByTagName("html")[0]),i=new MutationObserver(function(e){r.call(this,e,n)});var c=t(n.options);i.observe(l,c),n.observer=i,n.me=o}),i.beforeRemoving(function(e){e.observer.disconnect()}),this.bindEvent=function(e,t,n){t=l.mergeArrays(a,t);for(var r=l.toElementsArray(this),o=0;o<r.length;o++)i.addEvent(r[o],e,t,n)},this.unbindEvent=function(){var e=l.toElementsArray(this);i.removeEvent(function(t){for(var r=0;r<e.length;r++)if(this===n||t.target===e[r])return!0;return!1})},this.unbindEventWithSelectorOrCallback=function(e){var t,r=l.toElementsArray(this),o=e;t="function"==typeof e?function(e){for(var t=0;t<r.length;t++)if((this===n||e.target===r[t])&&e.callback===o)return!0;return!1}:function(t){for(var i=0;i<r.length;i++)if((this===n||t.target===r[i])&&t.selector===e)return!0;return!1},i.removeEvent(t)},this.unbindEventWithSelectorAndCallback=function(e,t){var r=l.toElementsArray(this);i.removeEvent(function(i){for(var o=0;o<r.length;o++)if((this===n||i.target===r[o])&&i.selector===e&&i.callback===t)return!0;return!1})},this},s=function(){function e(e){var t={attributes:!1,childList:!0,subtree:!0};return e.fireOnAttributesModification&&(t.attributes=!0),t}function t(e,t){e.forEach(function(e){var n=e.addedNodes,i=e.target,o=[];null!==n&&n.length>0?l.checkChildNodesRecursively(n,t,r,o):"attributes"===e.type&&r(i,t,o)&&o.push({callback:t.callback,elem:i}),l.callCallbacks(o,t)})}function r(e,t){return l.matchesSelector(e,t.selector)&&(e._id===n&&(e._id=o++),-1==t.firedElems.indexOf(e._id))?(t.firedElems.push(e._id),!0):!1}var i={fireOnAttributesModification:!1,onceOnly:!1,existing:!1};f=new a(e,t);var c=f.bindEvent;return f.bindEvent=function(e,t,r){n===r?(r=t,t=i):t=l.mergeArrays(i,t);var o=l.toElementsArray(this);if(t.existing){for(var a=[],s=0;s<o.length;s++)for(var u=o[s].querySelectorAll(e),f=0;f<u.length;f++)a.push({callback:r,elem:u[f]});if(t.onceOnly&&a.length)return r.call(a[0].elem,a[0].elem);setTimeout(l.callCallbacks,1,a)}c.call(this,e,t,r)},f},u=function(){function e(){var e={childList:!0,subtree:!0};return e}function t(e,t){e.forEach(function(e){var n=e.removedNodes,i=[];null!==n&&n.length>0&&l.checkChildNodesRecursively(n,t,r,i),l.callCallbacks(i,t)})}function r(e,t){return l.matchesSelector(e,t.selector)}var i={};d=new a(e,t);var o=d.bindEvent;return d.bindEvent=function(e,t,r){n===r?(r=t,t=i):t=l.mergeArrays(i,t),o.call(this,e,t,r)},d},f=new s,d=new u;t&&i(t.fn),i(HTMLElement.prototype),i(NodeList.prototype),i(HTMLCollection.prototype),i(HTMLDocument.prototype),i(Window.prototype);var h={};return r(f,h,"unbindAllArrive"),r(d,h,"unbindAllLeave"),h}}(window,"undefined"==typeof jQuery?null:jQuery,void 0);

/* ======= CODE ======== */

// Add custom style tag to document for CSS customization
let style = document.createElement('style');
let baseStyle = `
.path-highlighted .rm-bullet .rm-bullet__inner,
.path-highlighted .rm-bullet .rm-bullet__inner--user-icon {
    background-color: ${bulletColor} !important;
    transform: scale(${scale});
}
`
if(highlightRefs) {
  baseStyle += `
.path-highlighted + .roam-block .rm-page-ref,
.path-highlighted + .roam-block .rm-alias {
	color: ${refColor};
}
.path-highlighted + .roam-block .rm-block-ref {
	border-bottom-color: ${refColor};
}
`
}
style.textContent = baseStyle
document.body.appendChild(style);

// Remove classes when block is unfocused
document.leave('textarea.rm-block-input', function(el) {
    let bullets = [].slice.call(document.querySelectorAll('.path-highlighted'));

    bullets.forEach(function(bullet) {
        bullet.classList.remove('path-highlighted');
    })
})

// Show highlighted bullets + path when block is focused
let pathid = 0;
document.arrive('textarea.rm-block-input', function(el) {
    let bullets = [];
    let block = el.closest('.roam-block-container');
    // iterate through parents and get bullet elements
    while(block) {
        bullets.push(block.querySelector('.controls'));
        block = block.parentElement.closest('.roam-block-container')
    }
    
    // bullet styles cannot be applied directly to the element because they are pseudotags
    // so we'll create a style string and add it to the style tag we created earlier
    let bulletStyle = ''
    bullets.forEach(function(bullet, i) {
        let lastBullet = i > 0 ? bullets[i-1] : null
        // give each bullet a special path identifier so that we can target it directly
        if(!bullet.dataset.pathidentifier) { bullet.dataset.pathidentifier = pathid++ }
        
        if(lastBullet != null && showLines == true) {
            let bboxA = lastBullet.getBoundingClientRect()
            let bboxB = bullet.getBoundingClientRect()

            bulletStyle += `
.path-highlighted[data-pathidentifier="${bullet.dataset.pathidentifier}"] .bp3-popover-target::before {
    content: "";
    position: absolute;
    top: 10px; left: 6px;
    width: ${bboxA.x-bboxB.x}px; height: ${bboxA.y-bboxB.y}px;
    border: ${lineWidth}px solid ${lineColor};
    border-right: none;
    border-top: none;
    border-bottom-left-radius: ${borderRadius}px;
    pointer-events: none;
    z-index: 11 !important;
}
`
        }
        
        // highlight bullet
        bullet.classList.add('path-highlighted')
    })
    
    // set content of style tag to include both the base styles from before and the bullet styles we just generated
    style.textContent = baseStyle + bulletStyle;
})```
