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
    - 在roam research中实现类似anki的间隔记忆
        - roam/sr
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
