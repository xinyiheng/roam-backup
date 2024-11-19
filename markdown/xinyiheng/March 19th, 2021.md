- {{roam/render: 
  ```javascript
  if (typeof window.ExcalidrawWrapper === 'undefined') {
    window.ExcalidrawConfig = {
      rootPath: 'https://roam-excalidraw.vercel.app/',
      channel: 'dist',
      cljCodeVersion: 'excalidraw.app.mvp.v07',
      DEBUG : false,
      sketchingUID : 'sketching',
      excalDATAUID : 'ExcalDATA',
      excalSVGUID  : 'ExcalSVG_',
      settingsUID  : 'ExcalSET_',
      log (...args) {console.log("<<< Roam-Excalidraw loader >>> ",...args)},
    }
  
    const addElementToPage = (element, tagId, typeT )=> {
      try { document.getElementById(tagId).remove() } catch(e){};  //Delete any existing reference
      Object.assign(element, { type:typeT, async:false, id:tagId } );
      document.getElementsByTagName('head')[0].appendChild(element);
    }
  
    ExcalidrawConfig.addScriptToPage = (tagId, script)=> {
      addElementToPage(Object.assign(document.createElement('script'),{src:script}) , tagId, 'text/javascript');
    }
  
    ExcalidrawConfig.addCSSToPage = (tagId, cssToAdd)=> {
      addElementToPage(Object.assign(document.createElement('link'),{href:cssToAdd, rel: 'stylesheet'} ) , tagId, 'text/css');
    }
  
    function getClojureNS(blockUID) {
      q = `[:find ?s . :where [?e :block/uid "${blockUID}"][?e :block/string ?s]]`;
      renderString = window.roamAlphaAPI.q(q);
      if(renderString != null) { 
        ptrn = /\(ns (.*)\s/g;
        let res = ptrn.exec(renderString);
        ExcalidrawConfig.log('loader.js','getClojureNS NS:',res);
        if(res == null) return '';
        return res[1];
      }
      ExcalidrawConfig.log('loader.js','getClojureNS NS is EMPTY');
      return '';
    } 
  
    ( async ()=>{
      ExcalidrawConfig.log('loader.js','rootPath:',ExcalidrawConfig.rootPath,'channel:',ExcalidrawConfig.channel,'debug?',ExcalidrawConfig.DEBUG);
        if (getClojureNS(ExcalidrawConfig.sketchingUID) != ExcalidrawConfig.cljCodeVersion) {
          ExcalidrawConfig.log('loader.js','Need to update CLJS script. Starting roam-excalidraw-cljs-loader');
          ExcalidrawConfig.addScriptToPage( 'roam-excalidraw-cljs-loader',  ExcalidrawConfig.rootPath + 'get_dev.php?c='+ExcalidrawConfig.channel);
        }
        else {
          ExcalidrawConfig.log('loader.js','cljs NS is up to date');
          delete ExcalidrawConfig.sketchingUID;
          delete ExcalidrawConfig.excalDATAUID;
        }
        
        ExcalidrawConfig.addScriptToPage ('roam-excalidraw-main',ExcalidrawConfig.rootPath+ExcalidrawConfig.channel+'/main.js?v='+ExcalidrawConfig.cljCodeVersion);
        ExcalidrawConfig.addScriptToPage ('roam-excalidraw-react','https://unpkg.com/react@17/umd/react.production.min.js');
        ExcalidrawConfig.addScriptToPage ('roam-excalidraw-reactdom','https://unpkg.com/react-dom@17/umd/react-dom.production.min.js');
        ExcalidrawConfig.addScriptToPage ('roam-excalidraw-excalidraw','https://unpkg.com/@excalidraw/excalidraw@0.7.0/dist/excalidraw.production.min.js');
        ExcalidrawConfig.addCSSToPage ('roam-excalidraw-css',ExcalidrawConfig.rootPath+ExcalidrawConfig.channel+'/style.css?v='+ExcalidrawConfig.cljCodeVersion);
    })();
    
    ExcalidrawConfig.log('loader.js','Terminating temporary objects variables, rootPath, channel, getClojureNS, cljCodeVersion');
  
    delete ExcalidrawConfig.rootPath;
    delete ExcalidrawConfig.channel;
    getClojureNS = undefined;
    delete ExcalidrawConfig.cljCodeVersion;
  };
  ```}}
    - {{roam/render: 
      ```clojure
      undefined
      ``` {:elements [{:y 82.04384994506836, :isDeleted false, :strokeStyle "solid", :roughness 1, :width 177.705078125, :type "rectangle", :strokeSharpness "sharp", :fillStyle "hachure", :angle 0, :groupIds [], :seed 704458640, :boundElementIds nil, :strokeWidth 1, :opacity 100, :id "uN-xw-22NV1N7q0W7DG7L", :strokeColor "000000", :x 326.8615417480469, :version 27, :backgroundColor "transparent", :versionNonce 640940912, :height 219.52777862548828} {:y 136.33333206176758, :baseline 22, :isDeleted false, :strokeStyle "solid", :roughness 1, :width 80, :type "text", :strokeSharpness "sharp", :fillStyle "hachure", :angle 0, :groupIds [], :seed 386076016, :fontFamily 1, :boundElementIds nil, :strokeWidth 1, :opacity 100, :id "WmPgMit5lI33a5eTJcv-D", :verticalAlign "top", :strokeColor "000000", :textAlign "left", :x 381, :fontSize 20, :version 20, :backgroundColor "transparent", :versionNonce 1613725584, :height 29, :text "一个文本"}], :appState {:currentItemFontFamily 1, :isBindingEnabled true, :currentItemRoughness 1, :zoom {:value 1, :translation {:x 0, :y 0}}, :zenModeEnabled false, :lastPointerDownWith "mouse", :isLibraryOpen false, :scrollX 0, :selectedElementIds {:kto1nIv-IDcTVAWkN731F true}, :scrolledOutside false, :scrollY 0, :exportBackground true, :showStats false, :suggestedBindings [], :name "trying", :viewBackgroundColor "ffffff", :currentItemFillStyle "hachure", :width 884.6666870117188, :shouldCacheIgnoreZoom false, :currentItemStrokeSharpness "sharp", :selectedGroupIds {}, :isRotating false, :pasteDialog {:shown false, :data nil}, :offsetLeft 13, :currentItemStrokeWidth 1, :currentItemBackgroundColor "transparent", :elementType "selection", :offsetTop 39.66666793823242, :exportWithDarkMode false, :currentItemTextAlign "left", :currentItemLinearStrokeSharpness "round", :currentItemOpacity 100, :exportEmbedScene false, :currentItemStrokeColor "000000", :isLoading false, :currentItemFontSize 20, :elementLocked false, :currentChartType "bar", :shouldAddWatermark false, :currentItemEndArrowhead "arrow", :appearance "light", :previousSelectedElementIds {}, :viewModeEnabled false, :isResizing false, :showHelpDialog false, :height 608, :currentItemStrokeStyle "solid", :cursorButton "up"}} }}
    - trying
