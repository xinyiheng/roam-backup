1. ### 界面逻辑
    - marginnote3有mac和ipad两个版本。分成了文档-学习-复习三个大步骤
    - 文档部分
        - 管理部分比较废材，我已经用devonthink来接管了。方法是把marginnote中pdf文件夹以[[快捷方式]]的方式（devontink-file-index files and folders）关联到devonthink里面了。这样，我可以通过devonthink向marginnote里面添加文件。
    - 学习部分
        - 学习板块核心是思维导图。每一个思维导图好像又被称为一个笔记本。这个笔记本的独特之处如下。
一个思维导图可以关联非常多个文档，并非一篇文档只能建立一个思维导图。这一点非常关键。我比较喜欢针对一个主题进行集中阅读。这样，有一个超大型的思维导图就非常好。
            - 整合了大纲视图，大纲中的内容也可以非常方便的拖拽来调整位置和逻辑关系。
            - 思维导图模式非常方便，可以随意调整结构。导图的来自文档的部分可以添加标签、评论。在ipad版本中，还可以手写评论，非常方便。
            - 思维导图中来自文档的内容都可以轻松关联到原文位置。
            - 思维导图支持不同的卡片合并，不必复制粘贴，感觉非常好。这一点只有scrivener当的中卡片可以实现。我一直非常希望实现这一点。然而，我使用思维导图工具无法实现这一点。心里有些痒痒。@标签：进步
                - 目前的解决方式是在mindnode中使用自定义触控板手势来替代复制和粘贴，左侧底部双击剪切，右侧底部双击粘贴，这样不用按ctrl+x和ctrl+v @标签：小技巧
    - 复习板块
        - marginnote的复习功能非常非常棒。
        - 可以直接导出为anki文件，结合anki使用。
        - 制作填空题格式非常容易。
2. ### 特色功能
    - 标题链接
        - marginnote3新功能“标题链接”有多好用？Via[marginnote3新功能“标题链接”有多好用？性感笔记，点击查词_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1ho4y1d7De/?spm_id_from=autoNext) [[20220118]] 上午9:33@评论:也就是说，mn中允许多张卡片共用一个标题，打开标题链接功能以后，同样标题的所有卡片都可以在一起显示。
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FhSkqGIfTNt.png?alt=media&token=06f37666-0357-4a25-b1d7-4d22dbd8d762)
        - 所谓标题链接外部字典，就是另一本书中也提到了你作为卡片标题的概念，就把那一本书的相关卡片也一起显示出来。
    - 双向链接
3. ### marginnote插件
    - [最新插件与自动化/插件发布区话题 - MarginNote 中文社区](https://bbs.marginnote.cn/c/script/mod/55) [[20210915]] 下午10:49
    - ohmyMN,卡片批量重命名#[[文件批处理的概念]]@评论:还有一个功能，设置卡片标题更方便了。
    - allinone，好像只比较适合ipad，作者解说太差了。
    - 🗒@评论:这些插件开发主要用到了[[JavaScript]]
4. ### 细节问题
    - [[同步]]的逻辑很奇葩，这让管理阅读文件变得非常困难。
        - 在mac中凡是用marginnote打开的文件都被保存到marginnote内置的文件夹中，这样，电脑中原本只有一份的文件A就新增了一份marginnote里面的副本A'。
        - 如果开启icloud同步功能，那么这份文本就会上传到icloud中，这样，又生成了一份副本A''。如果只把icloud中的文件删除，在客户端同步并不会删除客户端内部的文件。也就是说，icloud在这里更像是一个云盘而不是同步盘，icloud的内容可以下载到客户端，而直接删除icloud里面的内容不能删除客户端里面的文件。如果用ipad版本的marginnote再打开这份文本，那么又会在ipad当中生成一份副本A'''如果不想要这份文件了，只有同时删除这三个地方的副本才算真正删除干净。
    - 文件格式
支持PDF和epub格式的文件，不支持mobi、azw3这些亚马逊为kindle开发的格式，但是通过calibre可以很快地转换成为epub格式，所以，电子书的格式不会成为阅读障碍
5. #[[软件联动]]
    - marginote与roam research[[hongse]]
        - MarginNote ✖️ Roam Research 阅读笔记插件，直接保存任意笔记到 Roam Research，支持 URL 跳转追溯原文Via[MarginNote ✖️ Roam Research 阅读笔记插件，直接保存任意笔记到 Roam Research，支持 URL 跳转追溯原文_哔哩哔哩_bilibili](https://www.bilibili.com/video/bv1Tf4y1P7WH) [[20210915]] 下午10:50 @评论:吕立青这个插件我无法使用，一直加载不出来。类似的还有slidepad浏览器，我不知道是不是vpn的问题。虽然我一直可以用chrome科学上网。@评论:目前已经解决这个问题了，使用的是 速蛙云。
        - 要想保留在marginote整理好的结构，可以先用其自带的导出功能导出到印象笔记。但缺点是，不是每张卡片都带着链接，以后把卡片移到别的地方的时候就可能找不到出处。我一直喜欢带着出处，虽然可能实际意义不大，但是还是尊重内心的这种需求吧。
        - 还有一个方法可以保留每一张卡片跳转回marginote的链接，但是缺点是无法保留原来整理好的层级。不过，我觉得这种方法对我来说更有价值。因为，我通常还要在roam research整理导入的内容，原来的结构并不那么重要。
            - 具体方法有些复杂。用marginnote自带的导出，导出为word文档。在word文章中选中所有文本，点击列表格式，清除掉原来所有的层级关系。然后再另存为rtf文件。这样，从rtf中复制出来的内容就保留了链接，并且所有的卡片之间是平级的关系。
    - 我觉得更好的方法是一张一张导入marginnote的内容到roam research，因为批量导入并不代表复习过了所有内容。可以在复习的时候，一张一张导入。我用better touch tool和keyboard 联合设置了快捷方式，单击触摸板的左下角就可以从marginnote导入一张带着跳转链接的卡片。
    - marginnote与[[Mindnode]]
        - 转换最好在阅读完成之后进行，否则，marginnote新添加的内容还需要重新导入。
    - 我认为ipad端比较好用的pdf阅读器除了marginote以外还有[[Goodnotes]]和[[LiquidText]]
