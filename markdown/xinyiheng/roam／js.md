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
var d=document.getElementsByClassName("bp3-button bp3-minimal bp3-small bp3-icon-more");
d.setAttribute("id","123");```
    - 
