- workflows
    - #SmartBlock Decision Journal
        - No. 1 #decision-journal
            - `Time: <%TIMEAMPM%>`
            - Decision:
            - Content
                - The situation/context:
                - The problem statement or frame:
                - The variables that govern the situation include:
                - The complications/complexities as I see them:
                - Alternatives that were seriously considered and not chosen were:
                - Explain the range of outcomes:
                - What I expect to happen and the actual probabilities are:
                - The outcome:
            - Review
                - Date:
                - What happended
                - What did you learn
    - #SmartBlock Unsplash Import
        - <%CURRENTBLOCKREF:startBlock,false%><%NOBLOCKOUTPUT%><%JAVASCRIPTASYNC: ```javascript
// Settings
var accessKey = "enter your Unsplash api key here";
var mode = "query"; // query or random
var defaultQuery = "relaxed";
var width = "600";
var display = "landscape" // portrait, landscape or squarish
// End Settings
////////////////

var url = "https://api.unsplash.com/photos/random?client_id="+accessKey+"";
document.unsplashURL = "";

if (typeof accessKey != 'undefined') {
if (typeof mode != 'undefined') {	
	if (mode == "query") {
      var query = prompt("What mood | mode | theme do you want?", defaultQuery);	
      	url += "&query="+query+"";
    } else if (mode == 'random') {
    } else {
  		alert("Please set Preferred Output mode to query or random")
	}
} else {
  alert("Please set Preferred Output mode in settings")
}
if (typeof width != 'undefined') {
	url += "&w="+width+"";
}
if (typeof display != 'undefined') {
	if (display == "portrait") {
  		url += "&orientation=portrait";
	} else if (display == "squarish") {
  		url += "&orientation=squarish";
	} else if (display == "lanscape") {
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

$.ajax(settings).done(async function (response) {
  console.log(response);
  var jsonUnsplash = JSON.stringify(response);
  var unsplash = JSON.parse(jsonUnsplash);
  var string = "![]("+unsplash.urls.regular+")\n'"+query+"' Image by [["+unsplash.user.name+"]] at [Unsplash]("+unsplash.user.links.html+")";
  await roam42.common.updateBlock(startBlock, string, true);
});``` %>
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
- daily
    - scheduled
    - time
        - 22:00
    - latest
        - 432a8159-868f-4a76-9319-f2972be0e3da
    - latest
        - 97a10766-ea13-4c4d-b88c-858f50ab3271
- trigger
    - jj
- publish
    - token
    - display name
        - wang
- hot keys
- highlighting
