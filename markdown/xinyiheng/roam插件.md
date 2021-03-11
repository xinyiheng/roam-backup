- [[roam highlighter]]
    - [派评 | 近期值得关注的 App - 少数派](https://sspai.com/post/64268)
        - 小时前
        - 大家好，本期《派评》的主要内容有：
        - 大版本。 
        - 你可以在桌面端通过网页右侧的目录进行快速跳转，阅读你感兴趣的内容。如果发现了其它感兴趣的 App 或者关注的话题，也欢迎在评论区和我们进行讨论。
        - - 值得关注的 
        - 我们每天都会接触不少实用、有趣的新 App，也会关注到不少应用的更新动态。「派评」为你筛选这些 App 之后，将最值得关注的应用动态呈现给你。
        - 是一款可以帮助我们拆解目标、制定计划的小应用。
        - 在 Iter 当中，每一个项目都被具化为一段旅程，点击添加后，我们便可以开始分解目标、制定计划，Iter 目前默认支持将内容拆分为两个层级。Iter 提供了极为详细的示例项目来帮助用户学习应用的使用，同时，这个示例也是一次如何进行任务分解的生动教育。
        - ![](https://cdn.sspai.com/2020/12/28/article/663038236012632e5f0de0ac53eb6ec9?imageView2/2/w/1120/q/90/interlace/1/ignore-error/1)
        - 除了进行最基础的任务分解，按时执行任务也是必不可少的。针对每一个具体步骤，我们都可以为其设置详细的提醒时间，对于需要定期重复的步骤，我们还能为步骤自定义重复周期，每当我们完成一个小目标时，便能勾选相应的目标来及时更新目标状态。
        - - Fitness Totals：健身小部件，你今天走一万步了吗？ 
        - 平台： 
        - 年均值，或是上一周期的总体完成情况等，看看你在新的一年里是否有所懈怠。点击底部的分享按钮，还可以自动生成运动数据图，方便与他人分享。
        - ![](https://cdn.sspai.com/2020/12/28/article/c143d25b3f5129dac729343880062a09?imageView2/2/w/1120/q/90/interlace/1/ignore-error/1)
        - 应用售价元，作为单一功能的小组件应用，实在不算便宜。而且喜欢运动的人，应该有其他穿戴设备支持数据展示，又或是通过
        - 图像编辑 
        - [@huhuhang](https://sspai.com/u/huhuhang)：一直以来，Pixelmator Pro 都紧跟系统新特性发布重要更新，Pixelmator Pro 2.0.2 已经支持了 iOS 14.3 推出的 Apple ProRAW 格式。
- 导入文章
    - {{[[roam/js]]}}
        - ```javascript
var existing = document.getElementById("roamjs-article");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/article.js";
  extension.id = "roamjs-article";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}
```
- [[RoamPortal-Search]]可以展示概念之间的立体图，非常棒，我设置了#[[快捷方式]]ctrl+p
- {{[[roam/js]]}}
    - ```javascript
var existing = document.getElementById("timeline");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/timeline.js";
  extension.id = "timeline";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}
```
- [[roam toolkit]]很早就安装了，但是很少使用，最近知道了它可以把卡片以思维导图的方式展示出来，感觉很惊艳，可以使用。我设置了调出这个插件的#[[快捷方式]]ctrl+i
    - ```javascript
```
- {{[[roam/js]]}}
    - ```javascript
/*
 * credit to Dhrumil Shah (@wandcrafting) and Robert Haisfield (@RobertHaisfield)
 * for the original concept which was part of their RoamGames submission
 * and can be found at: https://www.figma.com/file/5shwLdUCHxSaPNEO7pazbe/
 *
 */

/* ======= OPTIONS ======== */
/* note: if you change these, reload the page to see the effect */

// BULLET
let scale = 2;
let bulletColor = '#FF0099';

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
    z-index: 999;
}
`
        }
        
        // highlight bullet
        bullet.classList.add('path-highlighted')
    })
    
    // set content of style tag to include both the base styles from before and the bullet styles we just generated
    style.textContent = baseStyle + bulletStyle;
})```
- 卡片写作，我最喜欢的主题# [[blck:green]]
- {{[[roam/js]]}}
    - ```javascript
const CARD_MODE_VERSION = 'gh-pages'
window.URLScriptServer = `https://cdn.jsdelivr.net/gh/JimmyLv/styled-roam@${CARD_MODE_VERSION}/`
var s = document.createElement('script')
	s.type = "text/javascript"
    s.src =  window.URLScriptServer + "js/index.js"
	s.async = true
document.getElementsByTagName('head')[0].appendChild(s)```
- {{[[roam/js]]}}
    - ```javascript
// ==UserScript==
// @name         Responsive YouTube with Timestamp Control for Roamresearch
// @author       Connected Cognition Crumbs <c3founder@gmail.com>
// @require 	 Roam42: Wait until Roam42 loads completely
// @version      0.3
// @description  Add timestamp controls to YouTube videos embedded in Roam and makes the player responsive. 
//               Parameters:
//               Shortcuts: for grabbing title and current time as a timestamp.
//               	grabTitleKey: if in a DIRECT child block of the YT video, 
//									grabs the title and paste it to the beginning of the current block.
//			grabTimeKey: if in ANY child blocks of the YT video, 
//									grabs the current time of the player and paste it to the beginning.
//		        Player Size: Video height and width when the right sidebar is closed. 
// @match        https://*.roamresearch.com
const ytParams = {
  //Player Size
  vidHeight : 480,
  vidWidth : 720,
  //Shortcuts
  grabTitleKey : 'alt+a t',
  grabTimeKey : 'alt+a n'
};

const players = new Map(); 

var ytReady = setInterval(() => {
  if(typeof(YT) == 'undefined' || typeof(YT.Player) == 'undefined') {
    const tag = document.createElement('script');
    tag.src = 'https://www.youtube.com/iframe_api';
    const firstScriptTag = document.getElementsByTagName('script')[0];
    firstScriptTag.parentNode.insertBefore(tag, firstScriptTag); 	
    clearInterval(ytReady);
  }
}, 1000); 

//Fill out the current block with the given text
function fillTheBlock(givenTxt){
  var setValue = Object.getOwnPropertyDescriptor(window.HTMLTextAreaElement.prototype, 'value').set;
  let newTextArea = document.querySelector("textarea.rm-block-input");               
  setValue.call(newTextArea,  givenTxt);
  var e = new Event('input', { bubbles: true });
  newTextArea.dispatchEvent(e);  	       
}

var mouseTrapReady = setInterval(() => {  
  if(Mousetrap === undefined) return;
  Mousetrap.bind(ytParams.grabTitleKey, async function(e) {   
    e.preventDefault()
    if (e.srcElement.localName == "textarea") {
      var container = e.srcElement.closest('.roam-block-container');
      var parContainer = container.parentElement.closest('.roam-block-container');        
      var myIframe = parContainer.querySelector("iframe");
      if(myIframe === null) return false;
      var oldTxt = document.querySelector("textarea.rm-block-input").value;                  
      var newValue = players[myIframe.id].getVideoData().title + " " + oldTxt;
      fillTheBlock(newValue);
    }
    return false;
  });	
  Mousetrap.bind(ytParams.grabTimeKey, async function(e) {   
    e.preventDefault()
    for (var plyId in players) {
          if(players[plyId].getPlayerState() == 1){
            var timeStr = new Date(players[plyId].getCurrentTime() * 1000).toISOString().substr(11, 8)
            var oldTxt = document.querySelector("textarea.rm-block-input").value;                  
            fillTheBlock(timeStr + " " + oldTxt);        
            return false;
          }
    }
    return false;
  });	
  clearInterval(mouseTrapReady);
}, 1000); 

 
const activateYtVideos = () => {
	if(typeof(YT) == 'undefined' || typeof(YT.Player) == 'undefined') return;
    Array.from(document.getElementsByTagName('IFRAME'))
        .filter(iframe => iframe.src.includes('youtube.com'))            
        .forEach(ytEl => {   
            if(ytEl.closest('.rm-zoom-item') !== null) {
            	return; //ignore breadcrumbs            
            }
            const block = ytEl.closest('.roam-block-container');          		
            if(ytEl.src.indexOf("enablejsapi") === -1){
              var ytId = extractVideoID(ytEl.src); 
              var frameId = "yt-" + ytEl.closest('.roam-block').id;
              ytEl.parentElement.id = frameId; 
              ytEl.remove();
              players[frameId] = new window.YT.Player(frameId, {
                height: ytParams.vidHeight,  	
                width: ytParams.vidWidth, 
                videoId: ytId
              });                        
              wrapIframe(frameId);
            } else {				                                      
              var frameId = ytEl.id				  
            }
            addTimestampControls(block, players[frameId]);   
            var sideBarOpen = document.getElementById("right-sidebar").childElementCount - 1;
            //Make iframes flexible
            adjustIframe(frameId, sideBarOpen);  
        });
};

const addTimestampControls = (block, player) => {
  if (block.children.length < 2) return null;
  const childBlocks = Array.from(block.children[1].querySelectorAll('.roam-block-container'));
  childBlocks.forEach(child => {
    const timestamp = getTimestamp(child);
    const buttonIfPresent = child.querySelectorAll('.timestamp-control')[0]
    if (buttonIfPresent) {
        buttonIfPresent.remove();
    }
    if (timestamp) { 
      addControlButton(child, () => player.seekTo(timestamp, true));
    }
  });
};
  
const adjustIframe = (frameId, sideBarOpen) => {
  var child = document.getElementById(frameId); //Iframe
  var par = child.parentElement;
  if(sideBarOpen){
    child.style.position = 'absolute';
    child.style.margin = '0px';
    child.style.border = '0px';
    child.style.width = '100%';
    child.style.height = '100%';
    child.style.borderStyle = 'inset';
    child.style.borderRadius = '25px';
    par.style.position = 'relative';
    par.style.paddingBottom = '56.25%';     
    par.style.height = '0px';
  } else {
    child.style.position = null;
    child.style.margin = '0px';
    child.style.border = '0px';        
    child.style.width = ytParams.vidWidth + 'px';
    child.style.height = ytParams.vidHeight + 'px';
    child.style.borderStyle = 'inset';
    child.style.borderRadius = '25px';
    par.style.position = null;
    par.style.paddingBottom = '0px';   
    par.style.height = ytParams.vidHeight + 20 + 'px';
  }
}
    
const wrapIframe = (frameId) => {
  var child = document.getElementById(frameId); //Iframe
  var par = document.createElement('div');
  child.parentNode.insertBefore(par, child);
  par.appendChild(child);
  child.style.position = 'absolute';
  child.style.margin = '0px';
  child.style.border = '0px';
  child.style.width = '100%';
  child.style.height = '100%';
  par.style.position = 'relative';
  par.style.paddingBottom = '56.25%';     
  par.style.height = '0px';
};
const getControlButton = (block) => block.querySelectorAll('.timestamp-control')[0];

const addControlButton = (block, fn) => {
  const button = document.createElement('button');
  button.innerText = '►';
  button.classList.add('timestamp-control');
  button.style.borderRadius = '50%';
  button.addEventListener('click', fn);
  const parentEl = block.children[0];
  parentEl.insertBefore(button, parentEl.querySelectorAll('.roam-block')[0]);
};

const getTimestamp = (block) => {
  const innerBlockSelector = block.querySelectorAll('.roam-block');
  const blockText = innerBlockSelector.length ? innerBlockSelector[0].textContent : '';
  const matches = blockText.match(/^((?:\d+:)?\d+:\d\d)\D/); // start w/ m:ss or h:mm:ss
  if (!matches || matches.length < 2) return null;
  const timeParts = matches[1].split(':').map(part => parseInt(part));
  if (timeParts.length == 3) return timeParts[0]*3600 + timeParts[1]*60 + timeParts[2];
  else if (timeParts.length == 2) return timeParts[0]*60 + timeParts[1];
  else return null;
};

const extractVideoID = (url) => {
  var regExp = /^(https?:\/\/)?((www\.)?(youtube(-nocookie)?|youtube.googleapis)\.com.*(v\/|v=|vi=|vi\/|e\/|embed\/\/?|user\/.*\/u\/\d+\/)|youtu\.be\/)([_0-9a-z-]+)/i;
  var match = url.match(regExp);
  if ( match && match[7].length == 11 ){
      return match[7];
  }else{
      return null; 
  }
};
  
setInterval(activateYtVideos, 1000);```
- page协同-好像是把所有的相同含义的词都统一替换成一个，我还没用过# [[blck:green]]
- {{[[roam/js]]}}
    - ```javascript
var existing = document.getElementById("page-synonyms");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/page-synonyms.js";
  extension.id = "page-synonyms";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}
```
- 把文字转换为类似ppt的演示文本# [[blck:green]] triger:presentation
- {{[[roam/js]]}}
    - ```javascript
var existing = document.getElementById("presentation");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/presentation.js";
  extension.id = "presentation";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}

	```
- 方便建立query# [[blck:green]] triger:query
- {{[[roam/js]]}}
    - ```javascript
var existing = document.getElementById("query-builder");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/query-builder.js";
  extension.id = "query-builder";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}
```
- 插入emoji# [[blck:green]]  
- {{[[roam/js]]}}
    - ```javascript
var existing = document.getElementById("emojis");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/emojis.js";
  extension.id = "emojis";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}
```
- 把数字转化为图表# [[blck:green]]  triger:chart/line/bar
- {{[[roam/js]]}}
    - ```javascript
var existing = document.getElementById("charts");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/charts.js";
  extension.id = "charts";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}
```
- map# [[blck:green]] triger:maps
- {{[[roam/js]]}}
    - ```javascript
var existing = document.getElementById("maps");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/maps.js";
  extension.id = "maps";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}
```
  
- ocr识别文字，不支持中文# [[blck:green]] triger:
- {{[[roam/js]]}}
    - ```javascript
var existing = document.getElementById("image-tagging");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/image-tagging.js";
  extension.id = "image-tagging";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}
```
- 提醒功能# [[blck:green]] triger：alert
- {{[[roam/js]]}}
    - ```javascript
var existing = document.getElementById("alert");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/alert.js";
  extension.id = "alert";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}
```
- 发现未连接的page# [[blck:green]]
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
- 以方括号触发的js插件来源：[roamjs docs](https://roamjs.com/docs/extensions/charts）# [[blck:red]]
- 思维导图# # [[blck:green]]
    - {{[[roam/js]]}}
        - ```javascript
var existing = document.getElementById("mindmap");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/mindmap.js";
  extension.id = "mindmap";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}
```
- 秘密花园
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
- {{[[roam/js]]}}
    - ```javascript
var cbw = document.createElement("script");
cbw.type = "text/javascript";
cbw.src = "https://gitmurf.github.io/masonry-vanilla/JS/cycleBlockWidth.js";
document.getElementsByTagName("head")[0].appendChild(cbw);```
