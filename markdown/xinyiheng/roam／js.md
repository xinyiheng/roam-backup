- ### Code
    - {{[[roam/js]]}}
        - ```javascript


;(()=>{
  
  if( typeof window.catominor_tags != 'undefined') return;

  window.catominor_tags = {};

  const scanTags = () => {
    document.querySelectorAll('[data-tag]').forEach( (element)=>{
      console.log("start");
      let divBlockTagAttributeArray;
      let divBlock = element.parentElement.parentElement;
      const tagAttribute = " " + element.getAttribute('data-tag') + " ";
      
      
      

      
      let divBlockTagAttribute = divBlock.getAttribute("data-tags");
      
      if (divBlockTagAttribute ==  null){
        divBlockTagAttributeArray = [];
      } else {
        
        divBlockTagAttributeArray = divBlockTagAttribute.split(","); 
      }
    
      let index;
	 
      if(element) {
        console.log(tagAttribute);
        let index = divBlockTagAttributeArray.indexOf(tagAttribute);
        if (index == -1) {
       			divBlockTagAttributeArray.push(tagAttribute);
   		 }
     
      } else {
         let index = divBlockTagAttributeArray.indexOf(tagAttribute);
		 if (index > -1) {
       			divBlockTagAttributeArray.splice(index, 1);
   		 }
         
        
        
      }
      console.log(divBlockTagAttributeArray);
      divBlock.dataset.tags = divBlockTagAttributeArray.join();
      divBlock.parentNode.parentNode.parentNode.dataset.tagsUp = " " + divBlockTagAttributeArray.join() + " ";
     // divBlock.parentNode.parentNode.parentNode.childNodes[0].dataset.tagsDown = divBlockTagAttributeArray.join();


      console.log(divBlock.dataset.tags);
  
    })
  }

  scanTags()
  var observerTags = new MutationObserver(scanTags);
  observerTags.observe(document.querySelector('#app'), {
    childList: true,
    subtree: true
  })

})();```
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
- 实验
    - {{[[roam/js]]}}
        - ```javascript
/*var shiyan = document.getElementsByClassName("bp3-button bp3-minimal bp3-small bp3-icon-more");
shiyan.setAttribute("shuxing","xinde")*/
var date = new Date();
var h = date.getHours();
        if (h <12){
            alert('早上好，开始奋斗的一天吧！');
        } else if (h <18) {
             alert('下午好，再接再厉！');
        } else {
            alert('欢迎回家，好好休息！');
        }


```
- rm-block-separatorVia[DevTools - roamresearch.com/](devtools://devtools/bundled/devtools_app.html?remoteBase=https://chrome-devtools-frontend.appspot.com/serve_file/@ff5c0da2ec0adeaed5550e6c7e98417dac77d98a/&panel=elements&dockSide=undocked) [[20210913]] 下午11:52rm-block-separatorVia[document.querySelector() - Web API 接口参考 | MDN](https://developer.mozilla.org/zh-CN/docs/Web/API/Document/querySelector) [[20210913]] 下午11:55
- 
