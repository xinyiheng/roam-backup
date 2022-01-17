- chrome插件商店中的插件
    - [[RoamPortal-Search]]可以展示概念之间的立体图，非常棒，我设置了#[[快捷方式]]ctrl+p
    - [[roam highlighter]]
    - [[roam toolkit]]很早就安装了，但是很少使用，最近知道了它可以把卡片以思维导图的方式展示出来，感觉很惊艳，可以使用。我设置了调出这个插件的#[[快捷方式]]ctrl+i
        - ```javascript
```
- [[roam extentions]]基本上都是以[[roam/js]]为开头的
    - ExtensionsVia[RoamJS Extensions](https://roamjs.com/extensions) [[20220117]] 上午10:21 @评论:这是最全的一个寻找roam插件的地方。
    - 其中有一个叫做roam42的最特别，它最早提出了[[SmartBlock]]的概念，后来被官方接纳，不过两者差别还不小。
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
    - [[roam/comments]]
        - [[June 16th, 2021]]
            - {{[[roam/js]]}}
                - 
    - ### Code
        - {{[[roam/js]]}}
            - ```javascript


;(()=>{
  
  if( typeof window.catominor_tags != 'undefined') return;

  window.catominor_tags = {};

  const scanTags = () => {
    document.querySelectorAll('[data-tag]').forEach( (element)=>{
      console.log("start");
      let divBlockTagAttributeArray;
      let divBlock = element.parentElement.parentElement;
      const tagAttribute = " " + element.getAttribute('data-tag') + " ";
      
      
      

      
      let divBlockTagAttribute = divBlock.getAttribute("data-tags");
      
      if (divBlockTagAttribute ==  null){
        divBlockTagAttributeArray = [];
      } else {
        
        divBlockTagAttributeArray = divBlockTagAttribute.split(","); 
      }
    
      let index;
	 
      if(element) {
        console.log(tagAttribute);
        let index = divBlockTagAttributeArray.indexOf(tagAttribute);
        if (index == -1) {
       			divBlockTagAttributeArray.push(tagAttribute);
   		 }
     
      } else {
         let index = divBlockTagAttributeArray.indexOf(tagAttribute);
		 if (index > -1) {
       			divBlockTagAttributeArray.splice(index, 1);
   		 }
         
        
        
      }
      console.log(divBlockTagAttributeArray);
      divBlock.dataset.tags = divBlockTagAttributeArray.join();
      divBlock.parentNode.parentNode.parentNode.dataset.tagsUp = " " + divBlockTagAttributeArray.join() + " ";
     // divBlock.parentNode.parentNode.parentNode.childNodes[0].dataset.tagsDown = divBlockTagAttributeArray.join();


      console.log(divBlock.dataset.tags);
  
    })
  }

  scanTags()
  var observerTags = new MutationObserver(scanTags);
  observerTags.observe(document.querySelector('#app'), {
    childList: true,
    subtree: true
  })

})();```
    - roam gallary
        - {{[[roam/js]]}}
            - ```javascript
/*
 * Viktor's Roam gallery PoC v0.2 
 * author: @ViktorTabori
 *
 * How to install it:
 *  - go to page [[roam/js]]
 *  - create a node with: {{[[roam/js]]}}
 *  - create a clode block under it, and change its type from clojure to javascript
 *  - allow the running of the javascript on the {{[[roam/js]]}} node
 *  - reload Roam
 *  - click on images
 *  - edit image url on mobile: click top right corner of image
 */
window.ViktorGallery = window.ViktorGallery || (function(){
 	var started = false;

 	start();

	return {
		started: started,
		start: start,
		stop: stop,
	};

	function start() {
		if (started) return;
		started = !started;

		'click touchstart touchmove touchend'.split(' ').forEach(type=>{
			console.log('gallery looking for',type);
			document.addEventListener(type, process);
		});

		// inject photoswipe
		addFile('script','src','https://viktoroam.glitch.me/photoswipe.4.1.3-Viktor.Tabori.js');
		addFile('script','src','https://cdnjs.cloudflare.com/ajax/libs/photoswipe/4.1.3/photoswipe-ui-default.min.js');
		addFile('link', 'href', 'https://cdnjs.cloudflare.com/ajax/libs/photoswipe/4.1.3/photoswipe.css', {rel:'stylesheet'});
		addFile('link', 'href', 'https://cdnjs.cloudflare.com/ajax/libs/photoswipe/4.1.3/default-skin/default-skin.css', {rel:'stylesheet'});

		// pswp modal initiate
		if (!document.querySelector('.pswp')) {
			var div = document.createElement('div');
			div.innerHTML = '<div class="pswp" tabindex="-1" role="dialog" aria-hidden="true"> <div class="pswp__bg"></div> <div class="pswp__scroll-wrap"> <div class="pswp__container"> <div class="pswp__item"></div> <div class="pswp__item"></div> <div class="pswp__item"></div> </div> <div class="pswp__ui pswp__ui--hidden"> <div class="pswp__top-bar"> <div class="pswp__counter"></div> <div class="pswp__preloader"> <div class="pswp__preloader__icn"> <div class="pswp__preloader__cut"> <div class="pswp__preloader__donut"></div> </div> </div> </div> </div> <div class="pswp__share-modal pswp__share-modal--hidden pswp__single-tap"> <div class="pswp__share-tooltip"></div> </div> <div class="pswp__caption"> <div class="pswp__caption__center"></div> </div> </div> </div> </div>';
			document.body.appendChild(div);
		}

		return true;
	}

	function stop() {
		if (!started) return;
		started = !started;

		'click touchstart touchmove touchend'.split(' ').forEach(type=>{
			document.removeEventListener(type, process);
		});

		return true;
	}

	function process(e) {
		var zoom = 3; // level of zoom on svg images
		var target = e.target;
		var path = e.path;
		window.domURL = self.URL || self.webkitURL || self;

		// if PhotoSwipe is not present
		if (typeof PhotoSwipe == 'undefined' || typeof PhotoSwipeUI_Default == 'undefined') return;

		// handle touch moving
		if (e.type == 'touchstart') {
			PhotoSwipe.target = target;
			return;
		}
		if (e.type == 'touchmove') {
			delete PhotoSwipe.target;
			return;
		}
		if (e.type == 'touchend' && !PhotoSwipe.target) return;

		// parse svg
		if (!path) {
			path = [];
			for (var node = target; node && node != document.body; node = node.parentNode) {
				path.push(node);
			}
		}
		var svg = (path.filter(elem=>elem.nodeName&&elem.nodeName.match(/^svg$/i)) || [undefined])[0];
			svg = path.filter(elem=>elem.classList&&elem.classList.contains('rm-mermaid')).length && svg || undefined;
		if (svg) {
			target = svg;
		}

		// only for images and SVGs
		if (!(target.nodeName == 'IMG' && target.classList.contains('rm-inline-img') || svg)) return;

		// 44x44px top right corner: edit, won't trigger gallery on mobile
		var rect = target.getBoundingClientRect();
		var x = e.pageX - rect.left;
		var y = e.pageY - rect.top;
		console.log(x,y, x>(rect.width-44) && y<44); // top right corner
		if (window.innerWidth<500 && x>(rect.width-44) && y<44) return; // we don't fire for top right corner for mobile

		// prevent click, so editing is not initiated
		console.log(e.type,target,e);
		e.preventDefault();
		e.stopPropagation();

		// init gallery
		window.pswp = window.pswp || document.querySelector('.pswp');
		var items = Array.from(document.querySelectorAll('img.rm-inline-img, .rm-mermaid svg')).map(function(v){
			var ret = {};
			// svg
			if (v.nodeName.match(/^svg$/i)) {
				v.style.backgroundColor = '#eee';
				//ret.src = 'data:image/svg+xml;base64,'+window.btoa(unescape(encodeURIComponent(v.outerHTML)));
				//ret.src = svgToTinyDataUri(v.outerHTML); // credit: @tigt_, https://github.com/tigt/mini-svg-data-uri
				//ret.html = v.outerHTML;
				//ret.src = domURL.createObjectURL(new Blob([v.outerHTML.replace(/<br>/g,'<br/>')], {type:"image/svg+xml;charset=utf-8"}));
				ret.svg = v.outerHTML;
				ret.src = 'svg';
				ret.w = v.viewBox.baseVal.width*zoom;
				ret.h = v.viewBox.baseVal.height*zoom;
			} else { // image
				ret.src = v.src;
				ret.w = v.naturalWidth;
				ret.h = v.naturalHeight;
			}
			ret.msrc = ret.src;
			ret.dom = v;
			return ret;
		});
		var current = items.findIndex(function(v){return v.dom==target});
		var option = {
			showAnimationDuration: 0,
		    history: false,
		    index: current,
		    getThumbBoundsFn: function(index) {
		    	try {
			        var pageYScroll = window.pageYOffset || document.documentElement.scrollTop,
			            rect = items[index].dom.getBoundingClientRect(); 
			        return {x:rect.left, y:rect.top + pageYScroll, w:rect.width};
			    } catch(_) {

			    }
		    }
		};
		var gallery = new PhotoSwipe( pswp, PhotoSwipeUI_Default, items, option);
		setTimeout(function(){
			gallery.init();
			gallery.listen('close', function() {
				items.forEach(function(e){
					if (e.src && e.src.match(/^blob:/i)) {
						domURL.revokeObjectURL(e.src); // cleanup of svg blob URLs
					}
				});
	        });
		}, 0);
	}


	// inject code to head
	function addFile(type,srcName,src,opt){
		if (Array.from(document.head.getElementsByTagName(type)).filter(s=>s[srcName]==src).length) {
			console.log('already loaded', src);
			return;
		}
		var file = document.createElement(type);
		file[srcName] = src;
		file.async = false;
		if (typeof opt == 'object') {
			for (var i in opt) {
				file[i] = opt[i];
			}
		}
		document.head.appendChild(file);
		console.log('added', src);
		return true;
	}
})();

```
    - 热力图-目前还不好用
        - {{[[roam/js]]}}
            - ```javascript
var existing = document.getElementById("roamjs-heatmap-main");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/heatmap/main.js";
  extension.id = "roamjs-heatmap-main";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}```
    - discourse graph
        - {{[[roam/js]]}}
            - ```javascript
var existing = document.getElementById("roamjs-discourse-graph-main");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/discourse-graph/main.js";
  extension.id = "roamjs-discourse-graph-main";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}
```
    - sidebar
        - {{[[roam/js]]}}
            - ```javascript
var existing = document.getElementById("roamjs-sidebar");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/sidebar.js";
  extension.id = "roamjs-sidebar";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}
```
    - 实验
        - {{[[roam/js]]}}
    - 秘密花园
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
