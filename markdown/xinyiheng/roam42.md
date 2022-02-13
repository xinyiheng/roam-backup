- 相同概念
    - SmartBlock
- {{{[[roam/js]]}}}
    - ```javascript
var existing = document.getElementById("roamjs-roam42-main");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/roam42/2022-01-30-06-41/main.js";
  extension.id = "roamjs-roam42-main";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}```
- roam42这个网站是[[roamhacker]]这个组织？个人？运作的，可以把他们理解为同一个人。
- 旗下有一个很重要的功能，叫做smart block。smart block Builders Guide
via[SmartBlocks Builders Guide](https://roamresearch.com/#/app/roamhacker/page/GH0401tnt)
[[20201229]] 上午9:37
- 可以把daily note专门作成一个弹窗，做法是在任何位置加入下面这句代码
    - #42Setting DailyNotePopup off
- {{[[roam/js]]}}
    - ```javascript
var existing = document.getElementById("roamjs-smartblocks-main");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/smartblocks/main.js";
  extension.id = "roamjs-smartblocks-main";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}```
