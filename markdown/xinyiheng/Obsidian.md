- ### 想要实现的功能
    1. 在[[ipad]]和mac同步obsidian
        - 使用的下面这个仓库。有时候会因为icloud同步速度较慢而导致数据不同步。[笔记](hook://file/L0Q13iqY1?p=aUNsb3Vkfm1kfm9ic2lkaWFuL0RvY3VtZW50cw==&n=%E7%AC%94%E8%AE%B0)
    2. #[[软件联动]] 把[[Roam Research]]中的文档通过[[github]]备份到本地，然后用[[hazel]]自动复制到另一个文件夹中，这个文件夹作为obsidian的仓库来使用。
        - 其实我用obsidian就可以实现查看中观图景，因为obsidian的graph图呈现方式比roam research要好得多。好像[[王树义]]老师的方法也就是通过obsidian来优化的。最后好像也是通过[[github]]来同步。我目前的方法只能实现从roam research到obsidian的单项同步，如果能够实现双向同步就完美了。以下方法也只能实现单项同步，目前来看，我自己想到的把roam research和[[Obsidian]]联动起来的方法最好。[[软件联动]]
    3. 新增了canvas功能，非常接近[[Heptabase]]的使用体验了。最近[[Obsidian]]出了一款白板插件，感觉可以取代heptabase
    4. 改变graph节点的颜色原来很简单。obsidian中的图谱使用的是[WebGL ](brain://api.thebrain.com/g7PXu0IyM0ucARb24SvxiA/wi2B8K0hK0aP6-YksheQVA/WebGL)技术，好像幕布中的思维导图也是用的这种技术。
        - 节点设置颜色的方法如图所示，Ob在0.12版本后就出了“颜色组”这个功能。
        - 首先在关系图的设置里点开“颜色组”，然后点击“新建颜色组”，通过不同的检索方式将节点分类，然后对分好类的颜色组上色就行了。
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2Fnr74QeftuU.png?alt=media&token=2d3fa0aa-d4eb-46bb-bc66-1fec6e1cf3bc)
        - 关系图谱Via[关系图谱 - Obsidian 中文帮助 - Obsidian Publish](https://publish.obsidian.md/help-zh/%E6%8F%92%E4%BB%B6/%E5%85%B3%E7%B3%BB%E5%9B%BE%E8%B0%B1) [[20220114]] 下午11:51@评论:关系图谱中的线的颜色也可以改变，但是官方并没有给出说明，参考这个就可以修改了。
    5. Obsidian提供了从其他工具[迁移过来的方法](https://forum.obsidian.md/t/meta-migration-workflows/15252)
    6. 卡片视图：以卡片的形式呈现每个笔记page。
    7. 一个新的主题，可以用卡片的形式展示笔记，我还没时间折腾。#[[卡片笔记]]
        - Via[kepano/obsidian-minimal](https://github.com/kepano/obsidian-minimal) [[20220114]] 下午10:59
    8. 分栏：[Obsidian 分栏-重新设计_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1qL4y147iU?p=1&share_medium=android&share_plat=android&share_session_id=e6fb1db1-228d-4cd2-aeba-99c33a863c69&share_source=GENERIC&share_tag=s_i&timestamp=1642344305&unique_k=400MQus) [[20220117]] 上午9:35@评论:这个也有分栏效果，看起来太像notion了，不错。不过这位up主还没有说明怎样实现，以后跟进吧。
    9. 如何修改obsidian的字体以及其他外观设置？
        - [如何使用 CSS 改出一个令我满意的 Obsidian 外观？ - 少数派](https://sspai.com/post/75363)
        - [Obsidian如何保存网页高亮和批注，我的自动化流程_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1LF411G7US/?p=1&share_medium=android&share_plat=android&share_session_id=0b2073bd-dc40-453d-89ca-f6ad3f15d14c&share_source=GENERIC&share_tag=s_i&timestamp=1649983085&unique_k=yi6BhnQ&vd_source=3d8ccab137cc879b5f9cbc14d68843ab)
        - obsidian主题设置 - 少数派  https://sspai.com/post/66281 
            - @评论:下载了主题之后，可以在文件夹里找到css文件，然后找到字体字段修改就可以了。我使用的字体是从typora找到的"PT Serif"
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FeWU5Y7lapY.png?alt=media&token=8964683c-5314-4b94-b904-3418ae3cfb7b)

    10. 如何修改obsidian 上[[excalidraw]]插件的字体？
        - Obsidian 的 Excalidraw 插件自定义中文字体Via[Obsidian 的 Excalidraw 插件自定义中文字体](https://www.uncoverman.com/excalidraw-plguin-in-obsidian-support-font-custom.html) [[20220413]] 17:11
    11. 建立并发布个人网站。[[Obsidian]]也可以，我看[[指导员吴刚]]就自己建立了一个网站
- ### 插件及功能
    - 看板视图：其实[[Roam Research]]和[[Obsidian]]也都具有看板功能
    - The Brain视图：[[Obsidian]]有一款插件，大体实现了the brain的效果，叫做[[Juggl]]
    - 让 Obsidian 更好用，这些社区插件值得试试Via[让 Obsidian 更好用，这些社区插件值得试试 - 少数派](https://sspai.com/post/66094) [[20220114]] 下午11:32
        - [玩转 Obsidian 08：利用 Dataview 打造自动化 HomePage - 少数派](https://sspai.com/post/73958)@评论:这个插件我感觉就像是query
    - 我的 Obsidian 工作流：模板+QuickAdd+Dataview 快速创建和自动索引 - 少数派 (https://sspai.com/post/68350)
    - 常用 Obsidian 处理中文长文？试试这些这些大幅提升体验的插件和代码片段Via[常用 Obsidian 处理中文长文？试试这些这些大幅提升体验的插件和代码片段 - 少数派](https://sspai.com/post/69628) [[20211104]] 下午1:35
    - [拒绝折腾伪需求，我最爱用的 Obsidian 实用插件推荐。 - 少数派](https://sspai.com/post/72426)
- #[[参考资料]]
    - obsidian@评论:官方参考资料，用graph图展示
via[Index - Obsidian Help - Obsidian Publish](https://publish.obsidian.md/help/Index)
[[20201231]] 下午12:11
    - 快速开始 Via[由此开始 - Obsidian 中文帮助 - Obsidian Publish](https://publish.obsidian.md/help-zh/%E7%94%B1%E6%AD%A4%E5%BC%80%E5%A7%8B) [[20220114]] 下午11:43 @评论:这个帮助文档做的太棒了。我的知识管理体系其实很大程度上就是要做成这样。#[[知识管理]] [[hongse]]
    - 少数派上的文章一览https://sspai.com/search/post/obsidian
