- {{[[roam/js]]}}
    - ```javascript
var existing = document.getElementById("roamjs-simpread-main");
if (!existing) {
    var extension = document.createElement("script");
    extension.src = "http://localhost:7026/roamjs/inject.js";
    extension.id = "roamjs-simpread-main";
    extension.async = true;
    extension.type = "text/javascript";
    document.getElementsByTagName("head")[0].appendChild(extension);
}```
