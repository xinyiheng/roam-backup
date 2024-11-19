- 通过调用API在不同的软件之间传递数据
- 使用示例：
    - 使用 Google App Script 每天定时将[[exist.io]] 的数据同步到 [[Coda]]。下面提供一段示例代码，把 Coda token，Exist token，doc id，table id 替换即可（由于笔者并没学过 JavaScript，代码难免写的不符合规范，而且仅在笔者自己的测试中通过，还希望各位大佬指导改进）。
      
      CodaAPI.authenticate('[your Coda token]');function exist2coda()
      {  var existUrl='http://exist.io/api/1/users/$self/today/';  
      var options={    'method':'get',    headers:
      {      'Authorization':'Token [your exist token]'    },  }  
      var response=UrlFetchApp.fetch(existUrl, options);  
      var body = {  'rows': [    {'cells': [{'column': 'response', 
      'value': response.getContentText() }]    }]};  
      CodaAPI.upsertRows("DOC_ID", "TABLE_ID", body);}
      via[用 Coda 打造你的个人仪表盘 (3)--让量化自我不再繁琐 - 少数派](https://sspai.com/post/56565)
      [[20201224]] 下午10:34
    - 
- What Are APIs? - Simply ExplainedVia[(6) Are APIs? - Simply Explained - YouTube](https://www.youtube.com/watch?v=OVvTv9Hy91Q&feature=emb_rel_end)[[20210104]] 下午8:57
- 用网页访问本地文件
    - The File System Access API: simplifying access to local filesVia[The File System Access API: simplifying access to local files](https://web.dev/file-system-access/) [[20210215]] 下午11:25
