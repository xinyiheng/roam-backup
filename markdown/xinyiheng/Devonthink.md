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
- [DEVONthink Pro Office，文件管理爱好者的福音（一） - 少数派](https://www.diigo.com/outliner/diigo_items/1060283/12128769/485180111)
    - DEVONthink 的文件都在数据库里，并且只能由 DT 这个软件自身为入口去取用文件。少数情况下，因为没有 DT，即使有同步到坚果云，文件还是不可用。这个是我说的通用性的意思。GM 上面说的其实挺好，DT 的使用最好有个 主题，仅仅看作高级版 Finder 可能不是很适用。
    - DEVONthink Pro Office 本身就是一个文件管理器，升级版的 Finder，他对文件管理的组织性更加灵活，以我的观念来看，使用 DEVONthink Pro Office 最好有个「主题」，比如「外汇交易」，使用 DEVONthink Pro Office 把「外汇交易」相关的文本、知识、材料、PDF、数据、网页等等全部集合在一起，方便我们进一步学习和创作，如果没有相关的主题，那么整理文件就是整理文件而已。
    - 这其实就是通用性和功能性之间的矛盾，DT这类数据管理App是用所谓的「库文件」来实现数据管理，用户需要做的事情就是把数据放进去，进行各种数据相关操作的时候不需要考虑实际数据存储的结构，只需要做想做的事情就好了。这就把功能性和实际的文件数据结构之间独立开来了，用户只需要知道数据都在库文件里，需要的时候用DEVONthink这个入口进行访问，并不需要关心实际库文件里面复杂的数据标签关联的结构。当然这就带来了你提到的通用性问题，但是我认为这些文件数据重要的是你对它们进行的分类整理和其之间的各种关联关系，从这个角度来看，把各种文件和其分类整理和关联结构整体打包成一个库文件是更便利和方便的数据管理方式。同理，像照片App和iOS上的一些PDF阅读App（比如MarginNote和LiquidText）也是这样的库文件的使用方式。
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
    - 即使在不同的mac电脑之间，无法通过icloud之类的云同步工具来同步database。我目前的解决方案就是买了一个大容量的u盘，随身带着这个u盘。
