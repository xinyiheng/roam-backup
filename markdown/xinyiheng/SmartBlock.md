- 可以分为官方开发的和roam42这个民间开发的两种
- 官方开发的triger是;; 民间开发的triger是“jj”  
- 官方的模板都放在roam/templates这个page里面，而民间开发的都放在SmartBlock这个page里面
- 这种smart block可以在任何地方建立，只需要在一句话中用双方括号包住SmartBlock几个字就可以了。我统一放在这里是为了看上去整齐美观。
- smartblock自带的一些功能
    - 快速添加日期，比如，下周一
    - 查询todo，比如过期的或者没有时间的todo
    - block搜索，比如找到一些含有某些标签的block
    - 随机展示一个blcok
    - @评论:以上功能详见这篇文章USING PRE DEFINED WORKFLOWS😀😀Via[Using pre Defined workflows | Smartblocks](https://roamjs.com/extensions/smartblocks/using_pre-defined_workflows) [[20220117]] 下午12:42
- 自建SmartBlock工作流的一些参考资料
    - Block Related CommandsVia[Command reference | Smartblocks](https://roamjs.com/extensions/smartblocks/command_reference) [[20220117]] 下午12:44
    - 除了这些特殊的命令，还可以当做一个普通模板来使用
- #SmartBlock Random Poem
    - <%JAVASCRIPTASYNC:
      ```javascript
      
      return fetch("https://www.poemist.com/api/v1/randompoems")
      .then(r => r.json()).then(data => {
        document.poemData = data;
        console.log(data)
        return document.poemData[0].title + ' - [[' + document.poemData[0].poet.name + ']]'
      }).catch(e => e)
      ```%>
        - <%JAVASCRIPT: return document.poemData[0].content%>
- https://roamjs.com/extensions/smartblocks
- #SmartBlock Excalidraw
    - <%JA: 
      ```javascript
      const room = Array.from(window.crypto.getRandomValues(new Uint8Array(10))).map((byte) => `0${byte.toString(16)}`.slice(-2)).join("");
      const key = (await window.crypto.subtle.exportKey("jwk",await window.crypto.subtle.generateKey({name:"AES-GCM",length:128},true,["encrypt", "decrypt"]))).k;
      return `{{iframe: https://excalidraw.com/#room=${room},${key}}}`;
      ```%>
    - <%CURSOR%>
- #SmartBlock Excalidraw
    - Description
        - This smartblock will insert an iframe pointing to a unique Excalidraw collaboration room instance. This room is encrypted with a 128 bit AES-GCM key. Your drawing will be stored in an encrypted form on https://excalidraw.com 's servers. Currently Excalidraw will store your drawing indefinitely, but it is a good practice for important drawings to export the image and to store the file as well.
        - If you want to collaborate with others on the drawing, you can invite them by clicking the green collaboration icon and sharing the collaboration link with others. If you click Stop Session in the collaboration window, further changes to your drawing will no longer be saved, however those that have the link will continue to have access to the collaboration room. 
        - If you want to edit in full screen mode, simply copy the collaboration link, and open excalidraw in an new browser tab using the link.
        - If you see the number of collaborators increase, this is most likely a fantom effect. Close your excalidraw browser windows, navigate away from the page in Roam and back, and the number of collaborators should reset to 1.
        - If you like this script consider supporting me on https://ko-fi/zsolt
- #SmartBlock YouTube TimeStamp
    - {{Add Timestamp:42SmartBlock:YouTube TimeStamp:varYTbut=y}}
    - <%IFTRUE:"<%GET:varYTbut%>" == "y"%><%JAVASCRIPT:
      ```javascript
      if (window.YT !== undefined) {
          if (Array.from(document.getElementsByTagName('IFRAME')).filter(iframe => iframe.src.includes('youtube.com'))[0]) {
              var getClosestParent = function (elem, srcStr) {
                  for (; elem && elem !== document; elem = elem.parentNode) {
                      if (elem.getElementsByTagName('IFRAME').length > 0) {
                          var foundIframe = elem.getElementsByTagName('IFRAME')[0];
                          if (foundIframe.src.includes(srcStr)) { return foundIframe };
                      }
                  }
              };
              var ytIframe = getClosestParent(document.getElementsByTagName('TEXTAREA')[0], 'youtube.com');
              if (ytIframe) {
                  var ytIframeId = ytIframe.id;
                  var ytPlayer = YT.get(ytIframeId);
                  var currentTime = ytPlayer.getCurrentTime() - 5;
                  if (currentTime < 1) { currentTime = 1 };
                  return (new Date(currentTime * 1000).toISOString().substr(11, 8)) + ' - ';
              }
              else {
                  return "No YouTube Player Open!";
              }
          }
          else {
              return "No YouTube Player Open!";
          }
      }
      ```
      %><%CURSOR%>
    - <%IFTRUE:"<%GET:varYTbut%>" != "y"%> <%CURSOR%>
    - <%SET:varYTbut,n%><%NOBLOCKOUTPUT%>
- #[[SmartBlock]]flomo随机内容
    - <%SET:result,<%JA:
      ```javascript
      roam42.loader.addScriptToPage('turndown', 'https://unpkg.com/turndown/dist/turndown.js');
      var turndownService = new TurndownService();
      
      function getRandomInt(max) {
        return Math.floor(Math.random() * max);
      }
      
      const flomo_session = 'eyJpdiI6InRwOGJcLzB5OHhMbDR3S3ZINkl2OUNBPT0iLCJ2YWx1ZSI6IjA3cWhLenRyUXBsWG5ZTUQ0T2tIak1qam5sVlJRSzA5NDlHUDR0ZHBDVTVCMllEcGNoYURlQlRRb3czY1Z1R1AiLCJtYWMiOiJlYTgzMTIwNThkMzE1YzMyMWJiY2JiYzg2OGM5MWRmODNkNzA0Mjc0MTE5OWZiZWM0OWE4ZGYzOTRhM2MxOTMyIn0%3D'; // todo: update to your session key
      var text = '';
      var settings = {
        "url": `https://flomo-api-proxy.vercel.app/api/flomo?flomo_session=${flomo_session}`,
        "method": "GET",
        "timeout": 0,
        "async": false
      };
      
      await $.ajax(settings).then(function (response) {
        console.log({ response });
        const random = getRandomInt(response?.memos?.length);
        const resource = response?.memos[random]?.content;
        text = turndownService.turndown(resource)
      }).catch(error =>  console.info({ error }));
      return JSON.stringify({text});
      ```%>%><%J:return JSON.parse(result).text%>
