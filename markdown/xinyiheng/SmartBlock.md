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
    - <%JAVASCRIPTASYNC:```javascript

return fetch("https://www.poemist.com/api/v1/randompoems")
.then(r => r.json()).then(data => {
  document.poemData = data;
  console.log(data)
  return document.poemData[0].title + ' - [[' + document.poemData[0].poet.name + ']]'
}).catch(e => e)
```%>
        - <%JAVASCRIPT: return document.poemData[0].content%>
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
