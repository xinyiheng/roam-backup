- 这种smart block可以在任何地方建立，只需要在一句话中用双方括号包住并不42SmartBlock只几个字就可以了。我统一放在这里是为了看上去整齐美观。
- #42SmartBlock Random Quotes
    - <%NOBLOCKOUTPUT%><%JAVASCRIPTASYNC: ```javascript
var settings = {
  "url": "https://api.quotable.io/random",
  "method": "GET",
  "timeout": 0,
  "async": false
};

$.ajax(settings).done(function (response) {
  console.log(response);
  var jsonQuotes = JSON.stringify(response);
  var quote = JSON.parse(jsonQuotes);
  roam42.smartBlocks.activeWorkflow.vars['author'] = quote.author;
  roam42.smartBlocks.activeWorkflow.vars['quote'] = quote.content;
});
return '';``` %>
    - <%JAVASCRIPT: document.activeElement.value = ""; return'> ';%><%GET:quote%>
[[<%GET:author%>]]
- #42SmartBlock Random Poem
    - <%JAVASCRIPTASYNC:```javascript

return fetch("https://www.poemist.com/api/v1/randompoems")
.then(r => r.json()).then(data => {
  document.poemData = data;
  console.log(data)
  return document.poemData[0].title + ' - [[' + document.poemData[0].poet.name + ']]'
}).catch(e => e)
```%>
        - <%JAVASCRIPT: return document.poemData[0].content%>
- #42SmartBlock YouTube TimeStamp
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
