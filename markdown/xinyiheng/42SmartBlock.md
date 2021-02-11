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
- #42SmartBlock Useless Ideas 随机灵感
    -   <%NOBLOCKOUTPUT%><%JAVASCRIPTASYNC: ```javascript
  var settings = {
    "url": "https://q24.io/api/v1/idea",
    "method": "GET",
    "timeout": 0,
    "async": false
  };
  
  $.ajax(settings).done(function (response) {
    console.log(response);
    var jsonQuotes = JSON.stringify(response);
    var quote = JSON.parse(jsonQuotes);
    roam42.smartBlocks.activeWorkflow.vars['author'] = quote.author;
    roam42.smartBlocks.activeWorkflow.vars['quote'] = quote.idea;
    roam42.smartBlocks.activeWorkflow.vars['url'] = quote.url;
  });
  return '';``` %>
    - <%JAVASCRIPT: document.activeElement.value = ""; return'> ';%><%GET:quote%> [*](<%GET:url%>)
  [[<%GET:author%>]]https://www.youtube.com/watch?v=40uq4I40bWE&feature=emb_logo
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
- 这种[[smart block]]可以在任何地方建立，并不需要单独保存到这个page当中，我都统一放在这里是为了看上去整齐美观。
- [[roam research]]官方开发的[[smart block]]只能够放在roam/templatespage下才能调用。
- #42SmartBlock Unsplash
    - <%NOBLOCKOUTPUT%><%CLEARVARS%>
    - <%NOBLOCKOUTPUT%>
<%SET:accessKey,<%RESOLVEBLOCKREF:"n0yCij1SOF7C82IFHAZx3e29htwwnCL1Wc03a_23A60"%>%>
<%SET:mode,<%RESOLVEBLOCKREF:"QUERY"%>%><%SET:defaultQuery,<%RESOLVEBLOCKREF:"relaxed"%>%>
<%SET:width,<%RESOLVEBLOCKREF:"600"%>%>
<%SET:display,<%RESOLVEBLOCKREF:"LANDSCAPE"%>%>
    - <%NOBLOCKOUTPUT%><%JAVASCRIPTASYNC: ```javascript
var url = "https://api.unsplash.com/photos/random?client_id="+roam42.smartBlocks.activeWorkflow.vars["accessKey"]+"";
document.unsplashURL = "";

if (typeof roam42.smartBlocks.activeWorkflow.vars["accessKey"] != 'undefined') {
if (typeof roam42.smartBlocks.activeWorkflow.vars["mode"] != 'undefined') {	
	if (roam42.smartBlocks.activeWorkflow.vars["mode"] == "QUERY") {
      var query = prompt("What mood | mode | theme do you want?", roam42.smartBlocks.activeWorkflow.vars["defaultQuery"]);	
      	url += "&query="+query+"";
    } else if (roam42.smartBlocks.activeWorkflow.vars["mode"] == 'RANDOM') {
    } else {
  		alert("Please set Preferred Output mode to QUERY or RANDOM")
	}
} else {
  alert("Please set Preferred Output mode in settings")
}
if (typeof roam42.smartBlocks.activeWorkflow.vars["width"] != 'undefined') {
	url += "&w="+roam42.smartBlocks.activeWorkflow.vars["width"]+"";
}
if (typeof roam42.smartBlocks.activeWorkflow.vars["display"] != 'undefined') {
	if (roam42.smartBlocks.activeWorkflow.vars["display"] == "PORTRAIT") {
  		url += "&orientation=portrait";
	} else if (roam42.smartBlocks.activeWorkflow.vars["display"] == "SQUARISH") {
  		url += "&orientation=squarish";
	} else if (roam42.smartBlocks.activeWorkflow.vars["display"] == "LANDSCAPE") {
  		url += "&orientation=landscape";
	} 
}
} else {
  alert("Please enter Access Key in settings");
}

var settings = {
  "url": url,
  "method": "GET",
  "timeout": 0,
};

$.ajax(settings).done(function (response) {
  console.log(response);
  var jsonUnsplash = JSON.stringify(response);
  var unsplash = JSON.parse(jsonUnsplash);
  var string = "![]("+unsplash.urls.custom+")\nImage by [["+unsplash.user.name+"]] at [Unsplash]("+unsplash.user.links.html+")";
  let txtarea = document.activeElement;
  var setValue = Object.getOwnPropertyDescriptor(window.HTMLTextAreaElement.prototype, 'value').set;
  setValue.call(txtarea, string);
  const inputEvent = new Event('input', { bubbles: true })
  txtarea.dispatchEvent(inputEvent)
});``` %>
-  **Unsplash SmartBlock Configuration:**
    - **Mandatory Settings:**
        - *** Access Key:**
            - n0yCij1SOF7C82IFHAZx3e29htwwnCL1Wc03a_23A60
        - *** Preferred Search Mode:**    (QUERY)
            - QUERY
    -  **Optional Settings:**
        -  **Default Query:**    __(preferred default search term for prompt)__
            - relaxed
        - **Width:**    __(in pixels)__
            - 600
        - **Display:**    __(LANDSCAPE | PORTRAIT | SQUARISH)__
            - LANDSCAPE
- ## [[[[Algorithms of Thought]]/Difference Engine]]
    - #42SmartBlock Difference Engine
        - **Current Situation**
            - <%INPUT:__What__ is the current situation you want to change?%>
        - **Future Situation**
            - <%INPUT:__How__ would this situation look differently in the future?%>
        - **Differences**
            - <%INPUT:__What__ is one of the differences between your current and future situations?%>
            - {{Add another difference:42SmartBlock:zz Difference Engine - Add Difference}}
        - {{Finished adding differences:42SmartBlock:zz Difference Engine - Analysis}}
    - #42SmartBlock zz Difference Engine - Add Difference
        - <%NOBLOCKOUTPUT%><%SET:difference,<%INPUT:__What__ is another difference between your current and future situations?%>%>
        - <%JAVASCRIPT:
```javascript
document.activeElement.value = roam42.smartBlocks.activeWorkflow.vars["difference"];
return "";```%> <%FOCUSONBLOCK%> <%CURSOR%>
        - {{Add another difference:42SmartBlock:zz Difference Engine - Add Difference}}
    - #42SmartBlock zz Difference Engine - Analysis
        - <%JAVASCRIPT:
```javascript
document.activeElement.value = "**Most serious difference**";
return "";```%> <%FOCUSONBLOCK%>
            - <%CURSOR%>
                - {{Create a plan to close the gap:42SmartBlock:zz Difference Engine - Gap Plan}}
            - {{Analyze another difference:42SmartBlock:zz Difference Engine - Additional Analysis}}
    - #42SmartBlock zz Difference Engine - Additional Analysis
        - <%JAVASCRIPT:
```javascript
document.activeElement.value = "(())";
return "";```%> <%FOCUSONBLOCK%>
            - {{Create a plan to close the gap:42SmartBlock:zz Difference Engine - Gap Plan}}
        - {{Analyze another difference:42SmartBlock:zz Difference Engine - Additional Analysis}}
    - #42SmartBlock zz Difference Engine - Gap Plan
        - <%JAVASCRIPT:
```javascript
document.activeElement.value = "**Steps to reduce difference**";
return "";```%> <%FOCUSONBLOCK%>
            - <%INPUT:__What__ is one thing you could do to reduce this difference?%>
            - {{Add another step:42SmartBlock:zz Difference Engine - Reduction}}
    - #42SmartBlock zz Difference Engine - Reduction
        - <%NOBLOCKOUTPUT%><%SET:step,<%INPUT:__What__ is another thing you could do to reduce this difference?%>%>
        - <%JAVASCRIPT:
```javascript
document.activeElement.value = roam42.smartBlocks.activeWorkflow.vars["step"];
return "";```%> <%FOCUSONBLOCK%>
        - {{Add another step:42SmartBlock:zz Difference Engine - Reduction}}
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
