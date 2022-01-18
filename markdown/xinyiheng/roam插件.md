- chrome插件商店中的插件
    - [[roam portal]]可以展示概念之间的立体图，非常棒，我设置了#[[快捷方式]]ctrl+p
    - [[roam highlighter]]
    - [[roam toolkit]]很早就安装了，但是很少使用，最近知道了它可以把卡片以思维导图的方式展示出来，感觉很惊艳，可以使用。我设置了调出这个插件的#[[快捷方式]]ctrl+i
        - ```javascript
```
- [[roam extentions]]基本上都是以[[roam/js]]为开头的
    - ExtensionsVia[RoamJS Extensions](https://roamjs.com/extensions) [[20220117]] 上午10:21 @评论:这是最全的一个寻找roam插件的地方。它还推出了一个叫做[[roam/js/marketplace]]的插件专门管理下载的插件，可以说层层嵌套了。
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
    - [Roam-Excalidraw Plugin MVP Release](https://www.zsolt.blog/2021/03/roam-excalidraw-plugin-mvp-release.html) [[20210319]] 下午8:42 @评论:这是一款可以绘制类似whiteboard的插件
        - {{[[roam/js]]}}
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
    - telegroam  @评论:从telegram中直接发信息同步到roam research
        - {{[[roam/js]]}}
            - ```javascript
/*
 * Copyright (c) 2021 Mikael Brockman
 *
 * See the LICENSE file (MIT).
 */

// we use an "immediately invoked function expression"
// so our declarations don't become global properties
// because that might conflict with other extensions
(function () {
  function massage(text) {
    text = text.replace(/\bTODO\b/, "{{[[TODO]]}}")
    return text
  }

  function findBotAttribute(name) {
    const BOT_PAGE_NAME = "Telegram Bot"

    let x = roamAlphaAPI.q(`[
      :find (pull ?block [:block/uid :block/string])
      :where
        [?page :node/title "${BOT_PAGE_NAME}"]
        [?block :block/page ?page]
        [?block :block/refs ?ref]
        [?ref :node/title "${name}"]
        [?block :block/string ?string]
    ]`)

    if (!x.length) {
      throw new Error(`attribute ${name} missing from [[${BOT_PAGE_NAME}]]`)
    }

    return {
      uid: x[0][0].uid,
      value: x[0][0].string.split("::")[1].trim(),
    }
  }

  function uidForToday() {
    let today = new Date
    let yyyy = today.getFullYear()
    let mm = (today.getMonth() + 1).toString().padStart(2, '0')
    let dd = today.getDate().toString().padStart(2, '0')
    return `${mm}-${dd}-${yyyy}`
  }

  function formatTime(unixSeconds) {
    let date = new Date(1000 * unixSeconds)
    let hhmm = date.toLocaleTimeString("en-US", {
      hour12: false,
      hour: "2-digit",
      minute: "2-digit",
    })

    return hhmm
  }

  function stripTrailingSlash(url) {
    if (url.endsWith('/')) {
      return url.slice(0, -1)
    } else {
      return url
    }
  }

  let telegramApiKey = findBotAttribute("API Key").value

  function unlinkify(s) {
    if (s.match(/^\[.*?\]\((.*?)\)$/)) {
      return RegExp.$1
    } else {
      return s
    }
  }

  async function updateFromTelegram() {
    let corsProxyUrl =
      stripTrailingSlash(
        unlinkify(
          findBotAttribute("Trusted Media Proxy").value))
    let inboxName = findBotAttribute("Inbox Name").value
    let api = `https://api.telegram.org/bot${telegramApiKey}`

    let updateId = null
    let updateIdBlock = findBotAttribute("Latest Update ID")
    if (updateIdBlock.value.match(/^\d+$/)) {
      updateId = +updateIdBlock.value + 1
    }

    async function GET(path) {
      let response = await fetch(`${api}/${path}`)
      if (response.ok) {
        return await response.json()
      } else {
        throw new Error(`telegroam fetch: ${response.status}`)
      }
    }

    let updateResponse = await GET(`getUpdates?offset=${updateId}&timeout=60`)

    if (!updateResponse.result.length) {
      return
    }

    let dailyNoteUid = uidForToday()

    let inboxUid
    let inboxUids = roamAlphaAPI.q(`[
      :find (?uid ...)
      :where
        [?today :block/uid "${dailyNoteUid}"]
        [?today :block/children ?block]
        [?block :block/string "${inboxName}"]
        [?block :block/uid ?uid]
    ]`)

    if (inboxUids.length) {
      inboxUid = inboxUids[0]
    } else {
      inboxUid = roamAlphaAPI.util.generateUID()

      // put the inbox at the bottom of the daily note
      let order = findMaxOrder(dailyNoteUid) + 1
      roamAlphaAPI.createBlock({
        location: { "parent-uid": dailyNoteUid, order },
        block: { uid: inboxUid, string: inboxName }
      })
    }

    let maxOrder = findMaxOrder(inboxUid)

    let i = 1
    for (let result of updateResponse.result) {
      await handleTelegramUpdate(result, i)
      ++i
    }

    // Save the latest Telegram message ID in the Roam graph.
    let lastUpdate = updateResponse.result[updateResponse.result.length - 1]
    roamAlphaAPI.updateBlock({
      block: {
        uid: updateIdBlock.uid,
        string: `Latest Update ID:: ${lastUpdate.update_id}`
      }
    })

    function findMaxOrder(parent) {
      let orders = roamAlphaAPI.q(`[
        :find (?order ...)
        :where
          [?today :block/uid "${parent}"]
          [?today :block/children ?block]
          [?block :block/order ?order]
      ]`)

      let maxOrder = Math.max(-1, ...orders)
      return maxOrder
    }

    function createNestedBlock(parent, { uid, order, string, children = [] }) {
      if (uid === undefined) {
        uid = roamAlphaAPI.util.generateUID()
      }

      if (order === undefined) {
        order = findMaxOrder(parent) + 1
      }

      roamAlphaAPI.createBlock({
        location: { "parent-uid": parent, order },
        block: { uid, string }
      })

      for (let child of children) {
        createNestedBlock(uid, child)
      }

      return uid
    }

    function blockExists(uid) {
      return roamAlphaAPI.q(`[
        :find (?block ...)
        :where [?block :block/uid "${uid}"]
      ]`).length > 0
    }

    async function handleTelegramUpdate(result, i) {
      let { message, edited_message, poll } = result

      if (poll) {
        handlePollCreation()
      }

      if (edited_message && edited_message.location) {
        handleLiveLocationUpdate()
      }

      if (message) {
        handleMessage(message)
      }

      i++
      return i

      function handlePollCreation() {
        createNestedBlock(inboxUid, {
          order: maxOrder + i,
          string: `((telegrampoll-${poll - id}))`,
          children: [{
            string: "{{[[table]]}}",
            children: poll.options.map(({ option, i }) => ({
              string: `((telegrampoll-${poll.id}-${i}))`,
              children: [{
                string: `${option.voter_count}`
              }]
            }))
          }]
        })
      }

      function urlWithParams(url, params) {
        let qs = Object.entries(params).map(([k, v]) => `${k}=${v}`).join("&")
        return `${url}?${qs}`
      }

      function mapStuff({ latitude, longitude }) {
        let d = 0.004
        let bb = [longitude - d, latitude - d, longitude + d, latitude + d]
        let bbox = bb.join("%2C")
        let marker = [latitude, longitude].join("%2C")

        let osm = urlWithParams("https://www.openstreetmap.org/", {
          mlat: latitude,
          mlon: longitude
        })

        let gmaps = urlWithParams("https://www.google.com/maps/search/", {
          api: "1",
          query: `${latitude},${longitude}`
        })

        let url = urlWithParams(
          "https://www.openstreetmap.org/export/embed.html", {
            layer: "mapnik",
            bbox,
            marker
          })

        return {
          embed: `:hiccup[:iframe {
            :width "100%" :height "400"
            :src "${url}"
          }]`,
          osm: `[View on OpenStreetMap](${osm})`,
          gmaps: `[View on Google Maps](${gmaps})`,
        }
      }

      function makeLocationBlock(uid, location) {
        let mapuid = `${uid}-map`
        let { embed, osm, gmaps } = mapStuff(location)

        createNestedBlock(uid, {
          uid: mapuid,
          string: embed,
          children: [{
            uid: `${mapuid}-link-osm`,
            string: osm
          }, {
            uid: `${mapuid}-link-gmaps`,
            string: gmaps
          }]
        })
      }

      async function handleMessage() {
        let name = message.from ? message.from.first_name : null
        let hhmm = formatTime(message.date)
        let text = massage(message.text || "")

        if (message.location)
          text = "#Location"
        if (message.voice)
          text = "#Voice"
        if (message.video || message.video_note || message.animation)
          text = "#Video"
        if (message.photo)
          text = "#Photo"
        if (message.contact)
          text = "#Contact"

        let uid = `telegram-${message.chat.id}-${message.message_id}`

        console.log(message)

        let parent = inboxUid

        if (message.reply_to_message) {
          parent = [
            "telegram",
            message.reply_to_message.chat.id,
            message.reply_to_message.message_id,
          ].join("-")

          if (!blockExists(parent)) {
            // the message replied to is included in the reply
            // so we should use that
            // but for now we just make a placeholder
            createNestedBlock(inboxUid, {
              uid: parent,
              string: "[[Telegroam: placeholder for missing message]]"
            })
          }
        }

        createNestedBlock(parent, {
          uid,
          order: maxOrder + i,
          string: `[[${name}]] at ${hhmm}: ${text}`
        })

        async function insertFile(fileid, generate) {
          let photo = await GET(
            `getFile?chat_id=${message.chat.id}&file_id=${fileid}`)
          let path = photo.result.file_path
          let url = `https://api.telegram.org/file/bot${telegramApiKey}/${path}`

          let mediauid = createNestedBlock(uid, {
            string: generate(url)
          })

          let tmpuid = createNestedBlock(mediauid, {
            string: `Uploading in progress:: ${message.chat.id} ${fileid}`
          })

          console.log("fetching", url, "from proxy")
          let blobResponse = await fetch(
            `${corsProxyUrl}/${url}`
          )

          let blob = await blobResponse.blob()

          let ref = firebase.storage().ref().child(
            `imgs/app/${graphName()}/${mediauid}`
          )

          console.log("uploading", url, "to Roam Firebase")
          let result = await ref.put(blob)
          let firebaseUrl = await ref.getDownloadURL()

          roamAlphaAPI.updateBlock({
            block: {
              uid: mediauid,
              string: generate(firebaseUrl)
            }
          })

          roamAlphaAPI.deleteBlock({
            block: {
              uid: tmpuid
            }
          })
        }

        let photo = url => `![photo](${url})`
        let audio = url => `{{[[audio]]:${url}}}`
        let video = url => `:hiccup[:video {:controls true :src "${url}"}]`

        if (message.sticker) {
          if (message.sticker.is_animated)
            await insertFile(message.sticker.thumb.file_id, photo)
          else
            await insertFile(message.sticker.file_id, photo)
        }

        if (message.photo) {
          let fileid = message.photo[message.photo.length - 1].file_id
          await insertFile(fileid, photo)
        }

        if (message.voice) {
          await insertFile(message.voice.file_id, audio)
        }
        if (message.video) {
          await insertFile(message.video.file_id, video)
        }

        if (message.video_note) {
          await insertFile(message.video_note.file_id, video)
        }

        if (message.animation) {
          await insertFile(message.animation.file_id, video)
        }

        if (message.document) {
          await insertFile(message.document.file_id, url => `File:: [${message.document.file_name}](${url})`)
        }

        if (message.location) {
          makeLocationBlock(uid, message.location)
        }

        if (message.poll) {
          createNestedBlock(uid, {
            uid: `telegrampoll-${message.poll.id}`,
            order: 0,
            children: message.poll.options.map((option, i) => ({
              uid: `telegrampoll-${message.poll.id}-${i}`,
              order: i,
              string: option.text
            }))
          })
        }

        if (message.contact) {
          if (!message.contact.vcard) {
            let { first_name, last_name, phone_number } = message.contact

            let name = first_name
            if (last_name)
              name += ` ${last_name}`

            createNestedBlock(uid, [{
              string: `[[${name}]]`,
              children: [{
                string: `Phone Number:: ${phone_number}`
              }]
            }])
          }

          if (message.contact.vcard) {
            let vcard = parseVcard(message.contact.vcard)
            delete vcard.begin
            delete vcard.prodid
            delete vcard.version
            delete vcard.end

            if (vcard.fn)
              delete vcard.n

            let translations = {
              n: "Name",
              fn: "Full Name",
              email: "Email",
              tel: "Phone Number",
              adr: "Street Address",
              bday: "Birthday",
              impp: "Social Media",
            }

            console.log(vcard)

            createNestedBlock(uid, {
              order: 0,
              string: `[[${vcard.fn[0].value.trim()}]]`,
              children: Object.keys(vcard).map((k, i) => {
                let string = (translations[k] || k) + "::"

                let single = (
                  vcard[k].length == 1 && typeof vcard[k][0].value == "string"
                )

                if (single) {
                  string += " " + vcard[k][0].value.trim()
                }

                return {
                  order: i,
                  string,
                  children: !single ? [] : vcard[k].map(({ value }, j) => ({
                    order: j,
                    string: (
                      value instanceof Array
                        ? value.filter(x => x.trim()).join("\n")
                        : value.trim()
                    )
                  }))
                }
              })
            })
          }
        }
      }

      function handleLiveLocationUpdate() {
        let message = edited_message
        let uid = `telegram-${message.chat.id}-${message.message_id}`
        let mapuid = `${uid}-map`

        let { embed, osm, gmaps } = mapStuff(edited_message.location)

        roamAlphaAPI.updateBlock({
          block: {
            uid: mapuid,
            string: embed,
          }
        })

        roamAlphaAPI.updateBlock({
          block: {
            uid: `${mapuid}-link-osm`,
            string: osm
          }
        })

        roamAlphaAPI.updateBlock({
          block: {
            uid: `${mapuid}-link-gmaps`,
            string: gmaps
          }
        })
      }
    }
  }

  function sleep(s) {
    return new Promise(ok => setTimeout(ok, 1000 * s))
  }

  function hex(buffer) {
    return [...new Uint8Array(buffer)].map(
      x => x.toString(16).padStart(2, '0')
    ).join("")
  }

  async function hashString(string) {
    let hash =
      await crypto.subtle.digest("SHA-256",
        new TextEncoder("utf-8").encode(string))

    return hex(hash).substr(0, 16)
  }

  const lockStatus = {
    ok: 200,
    busy: 423,
  }

  let currentLockPath

  async function runWithMutualExclusionLock({ waitSeconds, action }) {
    let lockId =
      await hashString([graphName(), telegramApiKey].join(":"))

    let nonce =
      roamAlphaAPI.util.generateUID()

    let lockPath =
      `https://binary-semaphore.herokuapp.com/lock/${lockId}/${nonce}`

    let acquirePath = `${lockPath}/acquire`
    let releasePath = `${lockPath}/release`

    for (;;) {
      let result =
        await fetch(acquirePath, { method: "POST" })

      if (result.status === lockStatus.ok) {
        currentLockPath = lockPath

        try {
          return await action()
        } finally {
          console.log("telegroam: releasing lock")
          currentLockPath = null
          try {
            await fetch(releasePath, { method: "POST" })
          } catch (e) {
            console.error(e)
            throw e
          }
        }

      } else if (result.status === lockStatus.busy) {
        console.log(`telegroam: lock busy; waiting ${waitSeconds}s`)
        await sleep(waitSeconds)
      }
    }
  }

  async function updateFromTelegramContinuously() {
    for (;;) {
      try {
        let result = await runWithMutualExclusionLock({
          waitSeconds: 30,
          action: async () => {
            console.log("telegroam: lock acquired; fetching messages")
            return await updateFromTelegram()
          }
        })

      } catch (e) {
        console.error(e)
        console.log("telegroam: ignoring error; retrying in 30s")
        if (currentLockPath) {
          console.log("telegroam: releasing lock via beacon")
          navigator.sendBeacon(currentLockPath + "/release")
        }
        await sleep(30)
      }
    }
  }

  function graphName() {
    return document.location.hash.split("/")[2]
  }

  async function startTelegroam() {
    // We need to use the Firebase SDK, which Roam already uses, but
    // Roam uses it via Clojure or whatever, so we import the SDK
    // JavaScript ourselves from their CDN...

    if (document.querySelector("#firebase-script")) {
      okay()
    } else {
      let script = document.createElement("SCRIPT")
      script.id = "firebase-script"
      script.src = "https://www.gstatic.com/firebasejs/8.4.1/firebase.js"
      script.onload = okay
      document.body.appendChild(script)
    }

    async function okay() {
      if (firebase.apps.length == 0) {

        // This is Roam's Firebase configuration stuff.
        // I hope they don't change it.
        let firebaseConfig = {
          apiKey: "AIzaSyDEtDZa7Sikv7_-dFoh9N5EuEmGJqhyK9g",
          authDomain: "app.roamresearch.com",
          databaseURL: "https://firescript-577a2.firebaseio.com",
          storageBucket: "firescript-577a2.appspot.com",
        }

        firebase.initializeApp(firebaseConfig)
      }

      updateFromTelegramContinuously()
    }
  }

  startTelegroam()

  // The following VCard parser is copied from
  //
  //   https://github.com/Heymdall/vcard
  //
  // MIT License
  //
  // Copyright (c) 2018 Aleksandr Kitov
  //
  // Permission is hereby granted, free of charge, to any person
  // obtaining a copy of this software and associated documentation
  // files (the "Software"), to deal in the Software without
  // restriction, including without limitation the rights to use, copy,
  // modify, merge, publish, distribute, sublicense, and/or sell copies
  // of the Software, and to permit persons to whom the Software is
  // furnished to do so, subject to the following conditions:
  //
  // The above copyright notice and this permission notice shall be included
  // in all copies or substantial portions of the Software.
  //
  // THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
  // IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
  // FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
  // AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
  // LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
  // OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
  // SOFTWARE.
  //
  function parseVcard(string) {
    var PREFIX = 'BEGIN:VCARD',
      POSTFIX = 'END:VCARD';

    /**
     * Return json representation of vCard
     * @param {string} string raw vCard
     * @returns {*}
     */
    function parse(string) {
      var result = {},
        lines = string.split(/\r\n|\r|\n/),
        count = lines.length,
        pieces,
        key,
        value,
        meta,
        namespace;

      for (var i = 0; i < count; i++) {
        if (lines[i] === '') {
          continue;
        }
        if (lines[i].toUpperCase() === PREFIX || lines[i].toUpperCase() === POSTFIX) {
          continue;
        }
        var data = lines[i];

        /**
         * Check that next line continues current
         * @param {number} i
         * @returns {boolean}
         */
        var isValueContinued = function (i) {
          return i + 1 < count && (lines[i + 1][0] === ' ' || lines[i + 1][0] === '\t');
        };
        // handle multiline properties (i.e. photo).
        // next line should start with space or tab character
        if (isValueContinued(i)) {
          while (isValueContinued(i)) {
            data += lines[i + 1].trim();
            i++;
          }
        }

        pieces = data.split(':');
        key = pieces.shift();
        value = pieces.join(':');
        namespace = false;
        meta = {};

        // meta fields in property
        if (key.match(/;/)) {
          key = key
            .replace(/\\;/g, 'ΩΩΩ')
            .replace(/\\,/, ',');
          var metaArr = key.split(';').map(function (item) {
            return item.replace(/ΩΩΩ/g, ';');
          });
          key = metaArr.shift();
          metaArr.forEach(function (item) {
            var arr = item.split('=');
            arr[0] = arr[0].toLowerCase();
            if (arr[0].length === 0) {
              return;
            }
            if (meta[arr[0]]) {
              meta[arr[0]].push(arr[1]);
            } else {
              meta[arr[0]] = [arr[1]];
            }
          });
        }

        // values with \n
        value = value
          .replace(/\\n/g, '\n');

        value = tryToSplit(value);

        // Grouped properties
        if (key.match(/\./)) {
          var arr = key.split('.');
          key = arr[1];
          namespace = arr[0];
        }

        var newValue = {
          value: value
        };
        if (Object.keys(meta).length) {
          newValue.meta = meta;
        }
        if (namespace) {
          newValue.namespace = namespace;
        }

        if (key.indexOf('X-') !== 0) {
          key = key.toLowerCase();
        }

        if (typeof result[key] === 'undefined') {
          result[key] = [newValue];
        } else {
          result[key].push(newValue);
        }

      }

      return result;
    }

    var HAS_SEMICOLON_SEPARATOR = /[^\\];|^;/,
      HAS_COMMA_SEPARATOR = /[^\\],|^,/;
    /**
     * Split value by "," or ";" and remove escape sequences for this separators
     * @param {string} value
     * @returns {string|string[]
     */
    function tryToSplit(value) {
      if (value.match(HAS_SEMICOLON_SEPARATOR)) {
        value = value.replace(/\\,/g, ',');
        return splitValue(value, ';');
      } else if (value.match(HAS_COMMA_SEPARATOR)) {
        value = value.replace(/\\;/g, ';');
        return splitValue(value, ',');
      } else {
        return value
          .replace(/\\,/g, ',')
          .replace(/\\;/g, ';');
      }
    }
    /**
     * Split vcard field value by separator
     * @param {string|string[]} value
     * @param {string} separator
     * @returns {string|string[]}
     */
    function splitValue(value, separator) {
      var separatorRegexp = new RegExp(separator);
      var escapedSeparatorRegexp = new RegExp('\\\\' + separator, 'g');
      // easiest way, replace it with really rare character sequence
      value = value.replace(escapedSeparatorRegexp, 'ΩΩΩ');
      if (value.match(separatorRegexp)) {
        value = value.split(separator);

        value = value.map(function (item) {
          return item.replace(/ΩΩΩ/g, separator);
        });
      } else {
        value = value.replace(/ΩΩΩ/g, separator);
      }
      return value;
    }

    return parse(string)
  }

})()```
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
})
Search...
```
