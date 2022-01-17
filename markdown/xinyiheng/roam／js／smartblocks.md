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
    - #SmartBlock Weather Forecast
        - <%CURRENTBLOCKREF:wxHeader,false%><%NOBLOCKOUTPUT%><%JA:```javascript
// Settings
const wxSbName = "Weather Forecast";
const wxApiKey = "enter api key here";
var weatherDefaultLocation = "mel";
var weatherShortCodes = "mel: melbourne,au;"; 
var weatherDirectToDefault = "yes";
var wxUnits = "metric";
// End Settings
///////////////

/////////
// This is an updated version of the original code by David Eaton (eatondpe - https://github.com/eatondpe) with a full description at https://github.com/dvargas92495/SmartBlocks/issues/211.
// I don't deserve any credit for developing the code. I've just updated the SB to work for SmartBlock v2.
/////////

var wxLocation = window.localStorage.wxLocation;
if (typeof wxButton == 'undefined') {
  var wxButton;
}
let curBlockUid = await roam42.common.getDirectBlockParentUid(wxHeader);

function toSentenceCase (str) {
  if ((str===null) || (str==='')) {
       return;
  } else {
    str = str.​toString();
    return str.replace(/\w\S*/g, function(txt){return txt.charAt(0).toUpperCase() + txt.substr(1).toLowerCase();});
  }
}

/* load location short codes */
var wxShortCodes = function(){
  var result = {};
  weatherShortCodes.split(/\s*\;\s*/).forEach(function(el){ 
    var parts = el.split(/\s*:\s*/); result[parts[0]] = parts[1];
  });
  return result;
}();

/* get location for weather forecast */
switch (wxButton) {
  case "update":
    break;
  case "change":
    wxLocation = false;
    break;
  default:
    if (weatherDirectToDefault.toLowerCase() == 'yes') {
      wxLocation = weatherDefaultLocation;
    } else {
      wxLocation = false;
    }
}
if (!wxLocation) {
  var wxLocation = await smalltalk.prompt('title', 'What city? (ex. nyc or new york city,ny,us)',weatherDefaultLocation);
}

/* resolve location */
if (Object.keys(wxShortCodes).includes(wxLocation)) {
  wxLocation = wxShortCodes[wxLocation];
}

/* fetch weather forecast data */
var url = 'https://api.openweathermap.org/geo/1.0/direct?q='
    + wxLocation
    + '&limit=1&'
    + 'APPID=' + wxApiKey;
var requestResults = await fetch(url);
var dataResults = await requestResults.json();
var lat = dataResults[0].lat;
var lon = dataResults[0].lon;
if(dataResults[0].state) {
    var wxLocationName = dataResults[0].name + ', ' + dataResults[0].state + ' (' + dataResults[0].country + ')';
} else {
    var wxLocationName = dataResults[0].name + ' (' + dataResults[0].country + ')';
}
var url = 'https://api.openweathermap.org/data/2.5/onecall?'
    + 'lat=' + lat + '&lon=' + lon
    + '&units=' + wxUnits + '&'
    + 'exclude=minutely,hourly&'
    + 'APPID=' + wxApiKey;
var requestResults = await fetch(url);
var dataResults = await requestResults.json();
var curTimezone = new Date().getTimezoneOffset();
var weatherTimezone = dataResults.timezone_offset / 60 * -1;
var tzDiff = curTimezone - weatherTimezone;
var wxAlerts = '';

/* parse weather forecast data for each day */
/* Today */
var wxDay0 = '**' + dayjs(dataResults.daily[0].dt * 1000).format('dddd, MMM D, YYYY') + '**';
var wxConditions0 = dataResults.current.weather[0].main;
var wxDescriptionCur0 = toSentenceCase( dataResults.current.weather[0].description );
var wxDescription0 = toSentenceCase( dataResults.daily[0].weather[0].description );
var wxHighTemperature0 = Math.round(dataResults.daily[0].temp.max);
var wxLowTemperature0 = Math.round(dataResults.daily[0].temp.min);
var wxCurTemperature0 = Math.round(dataResults.current.temp);
var wxMorning0 = Math.round(dataResults.daily[0].temp.morn);
var wxAfternoon0 = Math.round(dataResults.daily[0].temp.day);
var wxEvening0 = Math.round(dataResults.daily[0].temp.eve);
var wxHumidity0 = Math.round(dataResults.current.humidity);
var wxPrecip0 = Math.round(dataResults.daily[0].pop * 100);
var wxSunrise0 = dayjs(dataResults.current.sunrise * 1000).add(tzDiff,'minute').format('h:mm A');
var wxSunset0 = dayjs(dataResults.current.sunset * 1000).add(tzDiff,'minute').format('h:mm A');
var wxWindSpeed0 = Math.round(dataResults.current.wind_speed);
/* Tomorrow */
var wxDay1 = '**' + dayjs(dataResults.daily[1].dt * 1000).format('dddd, MMM D, YYYY') + '**';
var wxDescription1 = toSentenceCase( dataResults.daily[1].weather[0].description );
var wxConditions1 = dataResults.daily[1].weather[0].main;
var wxHighTemperature1 = Math.round(dataResults.daily[1].temp.max);
var wxLowTemperature1 = Math.round(dataResults.daily[1].temp.min);
var wxMorning1 = Math.round(dataResults.daily[1].temp.morn);
var wxAfternoon1 = Math.round(dataResults.daily[1].temp.day);
var wxEvening1 = Math.round(dataResults.daily[1].temp.eve);
var wxHumidity1 = Math.round(dataResults.daily[1].humidity);
var wxPrecip1 = Math.round(dataResults.daily[1].pop * 100);
var wxSunrise1 = dayjs(dataResults.daily[1].sunrise * 1000).add(tzDiff,'minute').format('h:mm A');
var wxSunset1 = dayjs(dataResults.daily[1].sunset * 1000).add(tzDiff,'minute').format('h:mm A');
var wxWindSpeed1 = Math.round(dataResults.daily[1].wind_speed);
/* Day After Tomorrow */
var wxDay2 = '**' + dayjs(dataResults.daily[2].dt * 1000).format('dddd, MMM D, YYYY') + '**';
var wxDescription2 = toSentenceCase( dataResults.daily[2].weather[0].description );
var wxConditions2 = dataResults.daily[2].weather[0].main;
var wxHighTemperature2 = Math.round(dataResults.daily[2].temp.max);
var wxLowTemperature2 = Math.round(dataResults.daily[2].temp.min);
var wxMorning2 = Math.round(dataResults.daily[2].temp.morn);
var wxAfternoon2 = Math.round(dataResults.daily[2].temp.day);
var wxEvening2 = Math.round(dataResults.daily[2].temp.eve);
var wxHumidity2 = Math.round(dataResults.daily[2].humidity);
var wxPrecip2 = Math.round(dataResults.daily[2].pop * 100);
var wxSunrise2 = dayjs(dataResults.daily[2].sunrise * 1000).add(tzDiff,'minute').format('h:mm A');
var wxSunset2 = dayjs(dataResults.daily[2].sunset * 1000).add(tzDiff,'minute').format('h:mm A');
var wxWindSpeed2 = Math.round(dataResults.daily[2].wind_speed);

/* format weather cards */
/* day 0 */
var wxInfo0 = wxDay0 + '\n'
  +'**Currently: **'+wxDescriptionCur0+' ('+wxCurTemperature0+'°)\n'
  +'**Forecast: **'+wxDescription0+' ('+wxHighTemperature0+'°/'+wxLowTemperature0+'°)\n'
  +'**Morn: **'+wxMorning0+'° **Day: **'+wxAfternoon0+'° **Eve: **'+wxEvening0+'°\n'
  +'**Prec: **'+wxPrecip0+'% **Wind: **'+wxWindSpeed0+'mph **Hum: **'+wxHumidity0+'%'
  +' #wx-fc #weathercard #\[\[wx-'+wxConditions0+'\]\]';
/* day 1 */
var wxInfo1 = wxDay1 + '\n'
  +'\n'
  +'**Forecast: **'+wxDescription1+' ('+wxHighTemperature1+'°/'+wxLowTemperature1+'°)\n'
  +'**Morn: **'+wxMorning1+'° **Day: **'+wxAfternoon1+'° **Eve: **'+wxEvening1+'°\n'
  +'**Prec: **'+wxPrecip1+'% **Wind: **'+wxWindSpeed1+'mph **Hum: **'+wxHumidity1+'%'
  +' #wx-fc #weathercard #\[\[wx-'+wxConditions1+'\]\]';
/* day 2 */
var wxInfo2 = wxDay2 + '\n'
  +'\n'
  +'**Forecast: **'+wxDescription2+' ('+wxHighTemperature2+'°/'+wxLowTemperature2+'°)\n'
  +'**Morn: **'+wxMorning2+'° **Day: **'+wxAfternoon2+'° **Eve: **'+wxEvening2+'°\n'
  +'**Prec: **'+wxPrecip2+'% **Wind: **'+wxWindSpeed2+'mph **Hum: **'+wxHumidity2+'%'
  +' #wx-fc #weathercard #\[\[wx-'+wxConditions2+'\]\]';

/* remove previous weather forecast blocks */
await roam42.common.deleteBlock(wxHeader);
wxHeader = await roam42.common.createBlock(curBlockUid.parentUID,curBlockUid.order,'');

/* update header */
var wxUpdateTime = dayjs(dataResults.current.dt * 1000).format('h:mm A');
if (dataResults.alerts) {
  wxAlerts = '\n((\n'
    + dataResults.alerts[0].description.replace(/\n\*/g,'linebreak').replace(/\n/g,' ').replace(/linebreak/g,'\n*')
    + '))';
}
await roam42.common.updateBlock(wxHeader,
   '**'+wxLocationName+'** '
  +' __'+wxUpdateTime+'__ '
  +'\{\{ Update :SmartBlock:'+wxSbName
  +':wxButton=update\}\} '
  +'\{\{ Change :SmartBlock:'+wxSbName
  +':wxButton=change\}\} '
  + '   '+wxAlerts+' '
  +'#rm-grid #rm-grid-3c #.wx-header');

/* display weather cards */
await roam42.common.createBlock(wxHeader,0,wxInfo0);
await roam42.common.createBlock(wxHeader,1,wxInfo1);
await roam42.common.createBlock(wxHeader,2,wxInfo2);

/* save location for update action */
window.localStorage.setItem("wxLocation",wxLocation);
wxButton = '';

return '';```%>
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
    - token
    - display name
        - wang
- hot keys
- highlighting
