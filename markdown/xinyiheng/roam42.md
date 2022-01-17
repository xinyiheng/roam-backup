- 相同概念
    - 42SmartBlock，要想新增smartblock，就在42SmartBlock这个page下新增
- {{{[[roam/js]]}}}
    - ```javascript
var existing = document.getElementById("roamjs-roam42-main");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/roam42/main.js";
  extension.id = "roamjs-roam42-main";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}```
- roam42这个网站是[[roamhacker]]这个组织？个人？运作的，可以把他们理解为同一个人。
- smart block Builders Guide
via[SmartBlocks Builders Guide](https://roamresearch.com/#/app/roamhacker/page/GH0401tnt)
[[20201229]] 上午9:37
