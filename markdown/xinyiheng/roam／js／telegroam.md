- [[Telegram Bot]]
- {{roam/js}}
    - ```javascript
var existing = document.getElementById("telegroam");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://telegroam.vercel.app/main.js";
  extension.id = "telegroam";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}```
