- roam research 有可能用在哪些意想不到的方面？
    - [[出版]]行业  https://roamlibrary.com/library 好像运转的并不是很成功
    - [[知识服务]]https://twitter.com/Jimmy_JingLv/status/1338106648586379264?ref_src=twsrc%5Etfw
    - roam用于[[团队合作]]Roam for Teamwork
via[Roam for teamwork](https://roamforteamwork.com/)
[[20201230]] 下午11:00
    - 还有人专门做了网站教怎么使用roam research。https://www.effortlessoutput.com/
    - roam 共同读书活动总结的一些关键词https://twitter.com/liuyingyue/status/1338652103334629378?ref_src=twsrc%5Etfw
- #[[设计逻辑]]
    - page
    - block
        - [[block reference]]实际上是对于小的知识片段的重复引用。现在是每一段就是一个block
        - 通过缩进来确认的层级关系本来是一个语义群，我不妨称之为一个[[cluster]]，一个cluster是否可以当做一个block来处理呢？
    - graph
    - note
    - diagram
- #[[使用方法]]
    - [[视图]]丰富
        - diagram的使用方法@评论:这个功能还是挺好用的
            - How to build diagrams in Roam Research
via[How to build diagrams in Roam Research - Ness Labs](https://nesslabs.com/roam-research-diagrams)
[[20201223]] 下午10:50
            - {{[[diagram]]}}
                - 可以很方便地创建板块
                    - 只能显示一级内容，第二个层级的内容无法显示
                - 先把内容写下来然后在整理
                - 不仅可以写内容，还可以用箭头连接起来
                - 还可以用方框框起来
                - 还支持建立双向连接，识别双方括号标记
                - 还支持添加图片
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FkcJvNNtgKe.png?alt=media&token=678527b0-2637-4c76-b705-ed264c3f6025)
        - 表格视图
            - {{table}}
                - 标题
                    - 第一列
                        - 第二列
                            - 第三列
                                - 第四列
                - 第一行
                    - 好的
                        - 差的
                            - 
                                - 最差的
                - 第二行
                    - 新的
                        - 更新的
                            - 
                                - 最新的
                - 第三行
                    - 旧的
                        - 醉酒的
                            - 特别旧的
                                - 没用的
                - 第四行
                    - 坏的
                        - 生成很多
                            - 这样就可以成为表格了
        -  看板视图
            - {{[[kanban]]}}
                - 新的
                    - 应该可以继续使用下去
                    - 整合更加专业的工具
                    - 好像还是可以使用的
                    - 目录
                - 好的
                    - 作外接大脑12月新书推荐 | 29本好书，温暖你的冬天
via[卡片笔记](https://www.notion.so/b6dd6411de1d490fb7409e7f2d9ae32a?v=e8f1888c20594ba8a889f6c1da020bcb&p=811941f9344f4cc5afd435ce7a8f3395)
[[20201224]] 下午4:19
                - 差的
                    - 不错
        - 线路图
            - {{mermaid}}
                - graph TD;
    
                    - 开始-->途经1
    
                    - 途经1-->途经2
                    -  途经1-->途经3
                    - 途经3-->途经4
        - 花式样式
            - {{mermaid}}
                - journey
    title working day
    section Go to work
      Make tea: 5: Me
      Go upstairs: 3: Me
      Do work: 1: Me, Cat
    section Go home
      Go downstairs: 6: Me
      Sit down: 8: Me
        - 甘特图
            - {{mermaid}}
                - gantt
dateFormat  YYYY-MM-DD
title Adding GANTT diagram to mermaid
excludes weekdays 2014-01-10

section A section
Completed task            :done,    des1, 2014-01-06,2014-01-08
Active task               :active,  des2, 2014-01-09, 3d
Future task               :         des3, after des2, 5d
Future task2               :         des4, after des3, 5d 
    - [[roam research]]到底怎样整理？目前大多数都是标签概念的状态。整理成概念文档是否可以用[[query]]的方式。[[block reference]]之类的设计我算是彻底明白了原理。#[[概念区分]]
        - 复制一个block再粘贴到其他位置和[[block reference]]有什么区别？[[block reference]]和embed reference有什么区别？#[[概念区分]]
            - 复制block到一个新位置，如果block里有方括号括起来的概念，概念会和新位置page的标题建立关系，可以体现在#[[graph图]]中，而通过[[block reference]]而来的内容无法和新的page标题建立关系。比如下图中，蓝色字体部分是通过[[block reference]]方式建立的，红色方框框起来的概念没有体现在所在的page标题Inbox组成的图中。
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FQb1OpsYLbq.png?alt=media&token=9cd2330a-8eac-4ce1-ab9d-4e0df8d635d2)
            - 这么看起来，好像复制block更好，但是，block reference的好处是，双击reference可以跳转到block原来的地址，相当于一个快捷方式，是个分身，当原来内容变化的时候，分身也就变化了。不仅如此，block referenc可处理性更好，还可以转变为embed，或者是直接转变为文本，还可以选在带着子blcok。
        - block reference和embed的区别是embed可以带着子block，而reference原来是不能带子block，现在默认也是不带子block，不过现在也可以转变为带着子block的。
    - 我其实也可在大纲工具中的任何地方新建文档，只需要标注出它是关于这个主题的文档级别文件即可，以后通过搜索实现，或者是方便的时候再迁移到合适的笔记本当中。我关注的几个主题其实相当于笔记本。--这种说法在我当初想在[[diigo]]当中建立自己的[[知识体系]]的时候是成立的，但是在roam research当中就不成立了。因为在[[roam research]]中，生成graph的依据就是寻找page 的标题和该标题下的带有"[[]]'符号的的内容，并把他们做成graph，这种自动识别方式是无法识别出传统大纲视图下的层级隶属关系的。要想使用roam research 当中的graph，在做笔记的时候就必须遵守这种严格机械的规则啊。
    - 好像记录在[[roam research]] 中的文档再进一步整理的时候会有些复杂#[[问题]]#[[done]]
        - 我发现，在roam research中，如果想把一段文字移动到某个概念之下，只需要在这段文字中提到这个概念就可以了。这样，这段话肯定就可以通过link或者unlink的形式连接到这个概念之下了。如果想要移动到[[概念文档]]中也非常方便，只需要在这段话中提到这个概念并用双方括号括住这个概念，等概念变色之后，就说明连接已经建立，只需要shift+鼠标单击概念就可以在侧边栏打开概念文档，这样就可以把这段文字拖拽到概念文档中了。
    - [[块引用]]等于[[block reference]]复制一个block再粘贴到其他位置和[[block reference]]有什么区别？[[block reference]]和embed reference有什么区别？#[[概念区分]]
        - 首先就是要找到blcok在哪里。可能有两种情况，一种是将当前的block引用到别的地方。这种情况下，先copy block reference，然后再在搜索框中找到要放到的地方，粘贴就可以。
        - 另一种是要在当前block当中引用别的block，为了方便找到，可以通过以下方式实现
            - 将您的光标放在一个块中，然后按Ctrl-Shift-9弹出搜索框
- #[[快捷方式]]
    - 在windows 系统中，查看上一个或下一个page的按键是alt+左右箭头
    - 快速跳转到daily note ctrl+shift+d
    - 在[[roam research]]中打开开发者模式，ctrl+shift+=
- [[smart block]]是最近推出的杀手级的新功能，这让roam research有了更大的自定义的可能性。很多实现方式借助[[JavaScript]]
- #[[参考资料]]
    - Mickey Mellen  roam research的最近更新
-via[(880) Mickey Mellen - YouTube](https://www.youtube.com/c/mickmel/videos)
    - [官方论坛](https://forum.roamresearch.com/top/monthly)
    - https://roamdigest.com/#web@评论:内容很多
    - Roam Research 中文社区
via[roam 中文社区 ⛏🚀](https://roamresearchfan.com/)
[[20201214]] 下午8:22
    - Roam Newsletter 漫游研究所周报2020W51
via[](https://mp.weixin.qq.com/s/gxhCS42F981VzSb2-P9HZA)
[[20201228]] 下午4:34
    - [[twitter]]也是一种网状的组织结构
    - Roam中文站
via[Roam中文站的个人空间 - 哔哩哔哩 ( ゜- ゜)つロ 乾杯~ Bilibili](https://space.bilibili.com/599106362?spm_id_from=333.905.b_7570496e666f.3)
[[20201228]] 下午5:12
-  类似的软件
    - 可以参考别人列出的条目{{iframe: https://nano.page/page/roam}}
    - [[remnote]]
    - [[kanopi]]
    - [[swrite]]
    - [[hypernote]]
    - [[hypernotes]]和[[hypernote]]居然不是一个东西
    - [[hulunote]]
    - [[thinktool]]
    - [[tiddlywiki]]
    - [[logseq]]
    - [[wolai]]
    - [[roam edit]]
    - [[scrapbox]]
    - [[thinktool]]
    - [[innos note]]
    - 
- [[roam插件]]
    - [[roam portal]]
    - [[roam toolkit]]
    - [Roam-Excalidraw Plugin MVP Release](https://www.zsolt.blog/2021/03/roam-excalidraw-plugin-mvp-release.html) [[20210319]] 下午8:42 @评论:这是一款可以绘制类似whiteboard的插件
- roam research有哪些功能吸引了我？
    - 大网图、小网图（大纲/缩略式脑图）、大小粒度块引用、双向链接，是笔者认为的必备的四个双向链软件经典特征，其它就是附加插件功能，读者也可以从这四个经典元素对各种软件进行考察得出自己心中的排行，其实也就是Roam Research的核心功能。-20201027

作者：<em>[[威廉]]</em>
链接：https://zhuanlan.zhihu.com/p/267451435
via[(15 封私信 / 32 条消息) 威廉 obsidian - 搜索结果 - 知乎](https://www.zhihu.com/search?type=content&q=%E5%A8%81%E5%BB%89%20obsidian)
[[20201230]] 下午11:38
    - 因为笔者的时间认知有限有很多笔记只简单使用过如：[[Infranodus]]、[[xanadu]] space、wuli wiki、[[gource]]、notion、Athens Research、葫芦笔记、印象笔记、dynalist、thebrain、tiddlywiki、[[workflowy]]、雅典、Craft、marginnote、[[MyBase]]、[[swrite]]、trilium、gingko、WikiLinks、[[connected papers]]、tagspaces等。D3.js、neo4j、PowerBI、Charticulator、R语言、Phyone、Nvivo这些专业的大工具更是只有肤浅的了解，都还未进行深度使用所以不好进行排行和对比解读，也就没进行测评排行，更多的双向链笔记软件可能连名字都不知道，所以就未出现在此文。-

作者：<em>[[威廉]]</em>
链接：https://zhuanlan.zhihu.com/p/267451435
来源：知乎
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
via[(15 封私信 / 32 条消息) 威廉 obsidian - 搜索结果 - 知乎](https://www.zhihu.com/search?type=content&q=%E5%A8%81%E5%BB%89%20obsidian)
[[20201230]] 下午11:38
- #[[软件联动]]
    - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FMGOqbSgeQz.png?alt=media&token=8f895f65-b871-4b36-98e1-6fdf44df2dfd)
    - roam research如何与[[obsidian]]同步？#[[软件联动]]
        - 我自己也已经通过快捷方式可以让二者同步，也并不复杂，有空的时候再看看别人介绍的这个方法，好像[[github]]确实可以帮助完成很多事情。
        - @宽治：目前我就是 Roam Research（Web） 与 Obsidian （本地）两款软件并行的状况，这样做主要是想兼顾易用性和通用性：Roam Research 的交互方式用起来更加舒适，而以 markdown 文件为基础的 Obsidian 的通用性会更好。
目前，我在这两款工具的使用上，主要是做了一个内容方面的区分：偏研究性的内容会放在 Roam Research 上，偏写作类的内容会放在 Obsidian 上，而作为素材的笔记是用 Github 从 Roam Research 自动备份 再同步给 Obsidian 的。
via[Matrix 圆桌 | 网状结构笔记工具是一阵风吗？ - 少数派](https://sspai.com/post/61886)
[[20201213]] 上午7:52
    - 如何用roam research看中观图景？
        - 其实我用obsidian就可以实现查看中观图景，因为obsidian的graph图呈现方式比roam research要好得多。好像王树义老师的方法也就是通过obsidian来优化的。最后好像也是通过[[github]]来同步。我目前的方法只能实现从roam research到obsidian的单项同步，如果能够实现双向同步就完美了。以下方法也只能实现单项同步，目前来看，我自己想到的把roam research和[[obsidian]]联动起来的方法最好。[[软件联动]]
            - 在生活中，你用过导航吧？你如果想到一个 10 公里左右的目的地，导航会给你展示什么样的信息呢？世界地图？还是周围 5 米的区域？
都不是，应该先是一个从当前位置到目的地的概况图，之后给你展示清楚道路、红绿灯之类的动态视域。这就是合适的中观图。
你卡片足够多时， Roam Research 却偏偏还只给你展示全局链接图，这便本文开头我遇到的困境。
其实这个功能，并不难实现。在网络科学里面，这只是一个常见的「社区发现」（Community Detection）问题。
解决的算法，可以有很多。
我今天尝试了一下，用了最为应用广泛的 Louvain 方式，就可以立即把某个笔记节点所在的「社区」单独拿出来进行绘制。
via[如何交互可视化 Roam Research 局部笔记网络？ - 少数派](https://sspai.com/post/61864)
[[20201213]] 上午8:01
        - 「宏观」的全景图看不清，而「微观」的直接相连节点的图又过于狭窄，不利于我们看到笔记之间可贵的关联关系，尤其是那些「远程联想」，被时空关系切断了。要想看到它们、利用它们、让卡片之间发生「化学反应」，我们就需要一张「中观」图，既要有一定数量的笔记，帮助我们看到这种链接关系，又要避免过多的内容干扰我们的视域。
我做了个小工具，可以自动化对某一则笔记的「中观」图进行抽取和可视化，就像这个样子。希望看到这种有关联的「中观」网络图，你不必再有「密集恐惧症」的感叹了。
via[Matrix 圆桌 | 网状结构笔记工具是一阵风吗？ - 少数派](https://sspai.com/post/61886)
[[20201213]] 上午7:54
        - 这个网络不但可以交互显示，还支持点击直达具体的节点。而且因为一来本地操作，二来节点数量少了许多，图形处理的速度非常快捷。

而且，我们有了一个非常棒的临时工作空间。你可以在这里整合相关的卡片，进行项目级输出。然后把输出的结果反灌回 Roam Research ，作为当前上下文情境下的长期笔记。

我把上述功能对应的代码，开源托管在了 Github 。你可以在我的公众号「玉树芝兰」后台输入"louvain"获得代码。如果需要运行的话，你需要修改一下其中的 Roam Research 导出的 JSON，Markdown备份路径，Obsidian文件夹地址，以及你的种子笔记页面名称（qery_term）。

如果你熟悉前端，并且对这个功能比较感兴趣，欢迎进一步做个二次开发，让更多用户可以拿来即用。之前有不少小伙伴儿这么做了。例如最近，吕立青就把我之前做的 Roam Research 图片增量备份工具，集成到了 Roam to git 脚本里面，使得你可以完全用 Github 自动备份文字和图片内容，大伙儿用起来更加方便了。
via[如何交互可视化 Roam Research 局部笔记网络？ - 少数派](https://sspai.com/post/61864)
[[20201213]] 上午8:05
    - roam research的内容转换成为[[anki]]
    - 怎么修改roam research导出的文件的格式？
        - https://roam-tools.ryanguill.com/?这个网站可以实现一些修改。
- [Getting Started – Hook](https://hookproductivity.com/help/general/getting-started/#launch)
- [[间隔记忆]]
    - 目前roam research的插件也可以使用了，具体可以参考以下网页
        - https://roamstack.com/kb/extensions/roam-sr/#installing-roam-sr
