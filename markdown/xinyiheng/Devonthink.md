- #[[参考资料]]
    - [DEVONthink Pro Office，文件管理爱好者的福音（一） - 少数派](https://sspai.com/post/51242) 
    - 从 Evernote 到 DEVONthink
via[从 Evernote 到 DEVONthink - 少数派](https://sspai.com/post/44648)
[[20201220]] 上午7:45
        - 这些小书签只是一些简单的 JavaScript 代码，功能是获取一部分网页的属性，然后使用 URL Schemes 传入 DEVONthink。在 iOS 上有 Workflow，Mac 上有 Keyboard Maestro，小书签这个方法可以说已经完全过时了。
via[从 Evernote 到 DEVONthink - 少数派](https://sspai.com/post/44648)
[[20201220]] 上午7:46
        - DEVONthink 内包含了苹果的 WebKit 引擎，是有能力做一个浏览器的，其显示效果与当前版本的 Safari 保持一致。不同的是，DEVONthink 并不想把自己定位成普通[[浏览器]]，所以在 DEVONthink 中打开的网页是被当做一个个文档处理的，其地址栏无法用于导航，DEVONthink 的浏览功能定位是：获取、渲染、存储数据。DEVONthink 的浏览功能就是我指的「内部方法」，使用「内部方法」能很大程度上解决上述提到的问题。
via[从 Evernote 到 DEVONthink - 少数派](https://sspai.com/post/44648)
[[20201220]] 上午7:46
- devonthink的使用总算是入门了。
- 对标两个软件：
    - 印象笔记
    - mac中的finder
- 人工智能功能
    - 会根据导入的文件夹结构来自动创建一些tag
- 界面分成了inbox-database-group三个部分。
    - inbox就是把要整理的文档先放在这里。
    - 所有database共用一个inbox，旧版的是每个database都有一个自己的inbox。我觉得改的挺好。
    - database相当于一个非常大的文件夹
    - group是database下一级的文件夹
        - 还可以生产smart group，来方便提取和汇集文章。其实就是智能文件夹。
- 对导入devonthink中的文档添加很多信息，便于进一步加工。比如tag、lable，评分、作者等等信息。这也是^^smart group^^来分类的依据。
- smartgroup也可以当做保存特定搜索结果的方法
- 支持自动补全功能，用双方括号
- 也可以体现出双链
- 注意使用index files and folders来关联不愿意或者不能够加入到的devonthink中来的文件。这种文件再加上已经导入到devonthink中的文件，devonthink就可以全面接管本地文件。devonthink文件里删除的内容好像无法同步到finder的真实内容，但是文件夹之间的移动可以映射到真实的文件位置变动中。反过来，在真实文件夹的变动可以完全映射到devonthink当中。不过还要继续观察，我感觉过了一段时间以后，有些内容还是不一样了，不过我还没有确定。我猜测可能是devonthink数据库莫名其妙丢失之后，再重新打开就可能会发生这种情况。
- 我目前使用的几个主要功能
    - 电子书管理
        - 主要是可以[[全文搜索]]，即使是一些扫描的版本也可以。已经搜集了3000多本书。我实际上很少使用这一功能。
        - 我还比较喜欢其自带的[[词云图]]，但实际效果一般。所谓的[[词汇共现]]形成的网络看起来很酷炫，但是实际用途有限。
        - [[得到电子书]]和[[微信读书]]更实用一些
    - 剪藏网页
        - 剪藏网页可以保存为html格式，格式更接近原始界面。
- 重大缺陷
    - 所有保存在其中的电子书都是封装在一个devonthink的database里面的，即使同步windows电脑上，由于没有windows没有这个软件，无法打开查阅其中的内容。
    - ipad端做得也不好，这让devonthink只能够在mac电脑上使用。
