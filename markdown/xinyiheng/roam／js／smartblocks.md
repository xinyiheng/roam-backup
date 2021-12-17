- workflows
    - #SmartBlock Close Block Children
        - <%JAVASCRIPTASYNC:
```javascript
var parentBlock = document.activeElement.id.split('-').pop();
var thisBlockInfo = await roam42.common.getBlockInfoByUID(parentBlock);
var thisBlockInfoString = thisBlockInfo[0][0].string;

await roam42.common.updateBlock(parentBlock, thisBlockInfoString, false);```%><%NOBLOCKOUTPUT%>
    - #SmartBlock Create Numbered List
        - <%CURRENTBLOCKREF:parentBlockUID,false%><%NOBLOCKOUTPUT%><%JAVASCRIPTASYNC:
```javascript
var info = await roam42.common.getBlockInfoByUID(parentBlockUID, true, false);

var header = info[0][0].string;
if (header.match("xx")) {
	header = header.split("xx");
  	console.log(header);
} else if (header.match("{{")){
	header = header.split("{{");
  	console.log(header);
}

var headerText = header.trim();
headerText += "  {{Refresh Numbering:SmartBlock:Create Numbered List}}";
await roam42.common.updateBlock(parentBlockUID, headerText, true);

for (var i=0; i<info[0][0].children.length; i++) {
  const regex = /^\d.{0,10}: /;
  var numberSection = info[0][0].children[i].order +1;
  var blockTextString = info[0][0].children[i].string.replace(regex,"");
  var headerString = ""+numberSection+": "+blockTextString;
  await roam42.common.updateBlock(info[0][0].children[i].uid, headerString, true);
  if (info[0][0].children[i].hasOwnProperty('children')) {
    for (var j=0; j<info[0][0].children[i].children.length; j++) {
      var numberSubSection = info[0][0].children[i].children[j].order + 1;
  	  var blockTextSubString = info[0][0].children[i].children[j].string.replace(regex,"");
      var headerSubString = ""+numberSection+"."+numberSubSection+": "+blockTextSubString;
      await roam42.common.updateBlock(info[0][0].children[i].children[j].uid, headerSubString, true);
      if (info[0][0].children[i].children[j].hasOwnProperty('children')) {
        for (var k=0; k<info[0][0].children[i].children[j].children.length; k++) {
          var numberSubSubSection = info[0][0].children[i].children[j].children[k].order + 1;
  		    var blockTextSubSubString = info[0][0].children[i].children[j].children[k].string.replace(regex,"");
          var headerSubSubString = ""+numberSection+"."+numberSubSection+"."+numberSubSubSection+": "+blockTextSubSubString;
          await roam42.common.updateBlock(info[0][0].children[i].children[j].children[k].uid, headerSubSubString, true);
          if (info[0][0].children[i].children[j].children[k].hasOwnProperty('children')) {
            for (var l=0; l<info[0][0].children[i].children[j].children[k].children.length; l++) {
              var numberSubSubSubSection = info[0][0].children[i].children[j].children[k].children[l].order + 1;
  			      var blockTextSubSubSubString = info[0][0].children[i].children[j].children[k].children[l].string.replace(regex,"");
              var headerSubSubSubString = ""+numberSection+"."+numberSubSection+"."+numberSubSubSection+"."+numberSubSubSubSection+": "+blockTextSubSubSubString;
              await roam42.common.updateBlock(info[0][0].children[i].children[j].children[k].children[l].uid, headerSubSubSubString, true);
              if (info[0][0].children[i].children[j].children[k].children[l].hasOwnProperty('children')) {
                for (var m=0; m<info[0][0].children[i].children[j].children[k].children[l].children.length; m++) {
                  var numberSubSubSubSubSection = info[0][0].children[i].children[j].children[k].children[l].children[m].order + 1;
  				        var blockTextSubSubSubSubString = info[0][0].children[i].children[j].children[k].children[l].children[m].string.replace(regex,"");
                  var headerSubSubSubSubString = ""+numberSection+"."+numberSubSection+"."+numberSubSubSection+"."+numberSubSubSubSection+"."+numberSubSubSubSubSection+": "+blockTextSubSubSubSubString;
                  await roam42.common.updateBlock(info[0][0].children[i].children[j].children[k].children[l].children[m].uid, headerSubSubSubSubString, true);
                  if (info[0][0].children[i].children[j].children[k].children[l].children[m].hasOwnProperty('children')) {
                    for (var n=0; n<info[0][0].children[i].children[j].children[k].children[l].children[m].children.length; n++) {
                      var numberSubSubSubSubSubSection = info[0][0].children[i].children[j].children[k].children[l].children[m].children[n].order + 1;
                      var blockTextSubSubSubSubSubString = info[0][0].children[i].children[j].children[k].children[l].children[m].children[n].string.replace(regex,"");
                      var headerSubSubSubSubSubString = ""+numberSection+"."+numberSubSection+"."+numberSubSubSection+"."+numberSubSubSubSection+"."+numberSubSubSubSubSection+"."+numberSubSubSubSubSubSection+": "+blockTextSubSubSubSubSubString;
                      await roam42.common.updateBlock(info[0][0].children[i].children[j].children[k].children[l].children[m].children[n].uid, headerSubSubSubSubSubString, true);
                    }
                  }
                }
              }
            }
          }
        }
      }
    }
  }
}```%>
- trigger
    - jj
- publish
    - display name
        - wang
- hot keys
- highlighting
