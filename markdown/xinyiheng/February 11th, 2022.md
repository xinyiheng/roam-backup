- #[[写作]] #[[知识管理]] 把notion作为汇总写作文章之前的最终集合点。 
- #[[交互体验]] 为什么没有本质区别的东西会被人为看作不同的东西？#[[分列]]
    - A2画板 
    - 软木板
    - A2硬纸板
    - 办公桌的桌垫
    - 钢化玻璃白板
    - 桌子板面
    - 老式放在桌面上的玻璃
- #[[精力管理]] #[[知识管理]] 集中优势兵力消灭敌人有生力量
- #[[可视化]] #[[激励]] #[[理想]] 梦想画板
- #[[阅读管理]]
    - 知识管理流程中的阅读管理局部图 {{diagram}}
        - 阅读流程
        - 书籍
        - 一个概念
        - 一篇长文
        - 搜索
        - 另一本书
        - 下载
        - Devonthink
        - marginnote
        - roam research
        - 知识管理流程
        - diigo
- #[[知识表征]] #[[交互体验]] 就拿每天的活动来说，自己实际的生活是视频，但是用图片的方式呈现出来就很不容易了，更何况是文字。
    - ![photo](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FqvWTDu_rb?alt=media&token=c94feb7c-e615-4546-a27d-15274aff9e75)
- #[[知识管理]] #[[洞见]] 知识管理的核心就是把要整理的知识融入到自己的日程管理中。处理信息能力的带宽是很有限的，只有把材料放置到这个有限的区域之中，它才能够有可能成为有用的输出内容。
- #[[知识管理]] #[[洞见]] 材料+思维模型=知识
- #[[Roam Research]] #[[知识管理]] roam research或许也可以作为一个升级版本的diigo，汇总了很很多我要写作的素材和半成品，但总是感觉它无法承载最终的信息呈现。也就是不能作为一个很好的写作工具。 #[[知识表征]] 
- 了解[[视觉笔记]]，并在diigo中添加了几个专注于视觉笔记的公众号
- 想到利用[[幕布]]社区和其他拆书平台上别人整理的读书笔记来辅助自己建立知识体系。#[[知识管理]] 
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
      ``` {:appState {:currentItemFontFamily 1, :isBindingEnabled true, :currentItemRoughness 1, :zoom {:value 1, :translation {:x 0, :y 0}}, :zenModeEnabled false, :lastPointerDownWith "mouse", :isLibraryOpen false, :scrollX 0, :scrolledOutside false, :scrollY 0, :exportBackground true, :showStats false, :suggestedBindings [], :name "Untitled-2021-08-17-1714", :viewBackgroundColor "#ffffff", :currentItemFillStyle "hachure", :width 1129.630615234375, :shouldCacheIgnoreZoom false, :currentItemStrokeSharpness "sharp", :selectedGroupIds {}, :isRotating false, :pasteDialog {:shown false, :data nil}, :offsetLeft 16.988636016845703, :currentItemStrokeWidth 1, :currentItemBackgroundColor "transparent", :elementType "selection", :offsetTop 8.991477012634277, :theme "light", :exportWithDarkMode false, :currentItemTextAlign "left", :currentItemLinearStrokeSharpness "round", :currentItemOpacity 100, :exportEmbedScene false, :currentItemStrokeColor "#000000", :isLoading false, :currentItemFontSize 20, :elementLocked false, :currentChartType "bar", :shouldAddWatermark false, :currentItemEndArrowhead "arrow", :previousSelectedElementIds {}, :viewModeEnabled false, :isResizing false, :showHelpDialog false, :height 601.9885864257812, :currentItemStrokeStyle "solid", :cursorButton "up"}, :roamExcalidraw {:version 1}, :elements []} }}
    - **Text nested here will appear on your drawing:**
- #[[洞见]] #[[写作]] 我[[Roam Research]]做的这些笔记更像是在维护一个维基百科页面，而不像是真正的写作。
