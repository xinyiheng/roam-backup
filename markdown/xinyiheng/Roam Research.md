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
    - 设置css。如何在css block后面添加内容？ 例如，下面的第二个block怎么添加的？
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FpikCAarCOc.png?alt=media&token=6645b919-123d-4fa1-b34c-a0412a386ec5)
        - 点击css block区域，按住esc就可以显示原始代码，把光标放在最后处，按换行键就可以了。
    - [[视图]]丰富
        - diagram的使用方法@评论:这个功能还是挺好用的
            - How to build diagrams in Roam Research
              via[How to build diagrams in Roam Research - Ness Labs](https://nesslabs.com/roam-research-diagrams)
              [[20201223]] 下午10:50
            - {{[[diagram]]}}
                - 可很方便地创建板块
                    - 只能显示一级内容，第二个层级的内容无法显示
                - 先把内容写下来然后在整理
                - 可以写内容，还可以用箭头连接起来
                - 还可以用方框框起来
                - 还支持建立双向连接，识别双方括号标记
                - 还支持添加图片
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FkcJvNNtgKe.png?alt=media&token=678527b0-2637-4c76-b705-ed264c3f6025)
            - {{[[diagram]]}}
                - 新的内容
                - 尝试建立链接
                - 如何缩放大小
                - 如何退出全屏
                - 如何删除一个节点？
                - 建立这种方框好像还是用option键
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
        - 看板视图
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
    - [[Roam Research]]到底怎样整理？目前大多数都是标签概念的状态。整理成概念文档是否可以用[[query]]的方式。[[block reference]]之类的设计我算是彻底明白了原理。
      #[[概念区分]]
        - 复制一个block再粘贴到其他位置和[[block reference]]有什么区别？[[block reference]]和embed reference有什么区别？#[[概念区分]]
            - 复制block到一个新位置，如果block里有方括号括起来的概念，概念会和新位置page的标题建立关系，可以体现在#[[graph图]]中，而通过[[block reference]]而来的内容无法和新的page标题建立关系。比如下图中，蓝色字体部分是通过[[block reference]]方式建立的，红色方框框起来的概念没有体现在所在的page标题Inbox组成的图中。
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FQb1OpsYLbq.png?alt=media&token=9cd2330a-8eac-4ce1-ab9d-4e0df8d635d2)
            - 这么看起来，好像复制block更好，但是，block reference的好处是，双击reference可以跳转到block原来的地址，相当于一个快捷方式，是个分身，当原来内容变化的时候，分身也就变化了。不仅如此，block referenc可处理性更好，还可以转变为embed，或者是直接转变为文本，还可以选在带着子blcok。
        - block reference和embed的区别是embed可以带着子block，而reference原来是不能带子block，现在默认也是不带子block，不过现在也可以转变为带着子block的。
    - 我其实也可在大纲工具中的任何地方新建文档，只需要标注出它是关于这个主题的文档级别文件即可，以后通过搜索实现，或者是方便的时候再迁移到合适的笔记本当中。我关注的几个主题其实相当于笔记本。--这种说法在我当初想在[[Diigo]]当中建立自己的[[知识结构]]的时候是成立的，但是在roam research当中就不成立了。因为在[[Roam Research]]中，生成graph的依据就是寻找page 的标题和该标题下的带有"[[]]'符号的的内容，并把他们做成graph，这种自动识别方式是无法识别出传统大纲视图下的层级隶属关系的。要想使用roam research 当中的graph，在做笔记的时候就必须遵守这种严格机械的规则啊。
    - 好像记录在[[Roam Research]]中的文档再进一步整理的时候会有些复杂#问题#[[DONE]]
        - 我发现，在roam research中，如果想把一段文字移动到某个概念之下，只需要在这段文字中提到这个概念就可以了。这样，这段话肯定就可以通过link或者unlink的形式连接到这个概念之下了。如果想要移动到[[概念文档]]中也非常方便，只需要在这段话中提到这个概念并用双方括号括住这个概念，等概念变色之后，就说明连接已经建立，只需要shift+鼠标单击概念就可以在侧边栏打开概念文档，这样就可以把这段文字拖拽到概念文档中了。
    - [[块引用]]等于[[block reference]](c9nvg6Pgh)
        - 首先就是要找到blcok在哪里。可能有两种情况，一种是将当前的block引用到别的地方。这种情况下，先copy block reference，然后再在搜索框中找到要放到的地方，粘贴就可以。
        - 另一种是要在当前block当中引用别的block，为了方便找到，可以通过以下方式实现
            - 将您的光标放在一个块中，然后按Ctrl-Shift-9弹出搜索框
    - the brain和roam research的关系@评论:当the roam组织很好的时候，把二者关联起来，the brain就像是个非常好的概念图展示板，而展示的内容很多来自roam
    - 如何搜索和替换概念？
        - 并没有这个功能，echnique begins [2:13](https://www.youtube.com/watch?v=78p6z2104AU&t=133s)1. create Page with name equal to existing text you want to change2. Unlinked References > Link All3. rename Page to whatever you want   -------   4. delete Page Find and Replace Technique [[Roam Research]] - YouTube](https://www.youtube.com/watch?v=78p6z2104AU) [[20210712]] 上午9:01
    - 修改tag的样式
        - https://www.redgregory.com/roam-content/2021/1/8/customize-tags-inside-roam-research-with-this-simple-css
    - 如何在roam research中直接标注pdf？
        - 我觉得意义不大，没有实际使用，但是可以参考这个视频。
        - {{iframe:https://www.youtube.com/watch?v=g7iG47XeOX0}}
- #[[快捷方式]]
    - 在mac中，查看上一个或下一个用cmd+[或cmd+]，我现在才知道
    - 在windows 系统中，查看上一个或下一个page的按键是alt+左右箭头
    - 快速跳转到daily note ctrl+shift+d
    - {{iframe:https://cat-income-b7c.notion.site/f626dab7d985490fa504b763ea6f3e3c}}
    - 在[[Roam Research]]中打开开发者模式，ctrl+shift+=
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
    - [[Twitter]]也是一种网状的组织结构
    - Roam中文站
      via[Roam中文站的个人空间 - 哔哩哔哩 ( ゜- ゜)つロ 乾杯~ Bilibili](https://space.bilibili.com/599106362?spm_id_from=333.905.b_7570496e666f.3)
      [[20201228]] 下午5:12
-  类似的软件
    - 可以参考别人列出的条目{{iframe: https://nano.page/page/roam}}
    - [[Remnote]]
    - [[kanopi]]
    - [[swrite]]
    - [[hypernote]]
    - [[hypernotes]]和[[hypernote]]居然不是一个东西
    - [[hulunote]]
    - [[thinktool]]
    - [[tiddlywiki]]
    - [[Logseq]]
    - [[wolai]]
    - [[roam edit]]
    - [[scrapbox]]
    - [[thinktool]]
    - [[innos note]]
- [[Roam插件]]
- roam research有哪些功能吸引了我？
    - 大网图、小网图（大纲/缩略式脑图）、大小粒度块引用、双向链接，是笔者认为的必备的四个双向链软件经典特征，其它就是附加插件功能，读者也可以从这四个经典元素对各种软件进行考察得出自己心中的排行，其实也就是Roam Research的核心功能。-20201027
      作者：[[威廉]]
      链接：https://zhuanlan.zhihu.com/p/267451435
      via[(15 封私信 / 32 条消息) 威廉 obsidian - [[搜索]]结果 - 知乎](https://www.zhihu.com/search?type=content&q=%E5%A8%81%E5%BB%89%20obsidian)
      [[20201230]] 下午11:38
    - 因为笔者的时间认知有限有很多笔记只简单使用过如：[[Infranodus]]、[[xanadu]] space、wuli wiki、[[gource]]、notion、Athens Research、葫芦笔记、印象笔记、dynalist、thebrain、tiddlywiki、[[Workflowy]]、雅典、Craft、marginnote、[[MyBase]]、[[swrite]]、trilium、gingko、WikiLinks、[[connected papers]]、tagspaces等。D3.js、neo4j、PowerBI、Charticulator、R语言、Phyone、Nvivo这些专业的大工具更是只有肤浅的了解，都还未进行深度使用所以不好进行排行和对比解读，也就没进行测评排行，更多的双向链笔记软件可能连名字都不知道，所以就未出现在此文。
      
      作者：[[威廉]]
      链接：https://zhuanlan.zhihu.com/p/267451435
      来源：知乎
      via[(15 封私信 / 32 条消息) 威廉 obsidian - 搜索结果 - 知乎](https://www.zhihu.com/search?type=content&q=%E5%A8%81%E5%BB%89%20obsidian)
      [[20201230]] 下午11:38
- #[[软件联动]]
    - 如何用roam research模拟使用[[Heptabase]]的体验？
        - 用到两个功能，一个是插件[masonry-vanilla](https://github.com/GitMurf/masonry-vanilla)，另一个是roam自带diagram。在diagram中绘制一些想要关联的内容，用双方括号包裹起来，想要打开的时候就用shift点击，右侧就可以出现一张卡片。这样，既有卡片视图，也有卡片之间的联系。更为重要的是，卡片内部写的每个blcok也都可以被引用，所以，处理信息的颗粒度可以更小。
    - [Getting Started – Hook](https://hookproductivity.com/help/general/getting-started/#launch) 用这个软件可以把一些mac电脑中的其他文件以链接的形式添加到roam research中，这样可以完善它作为一元化笔记系统的核心处理器功能。#[[软件联动]]
    - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FMGOqbSgeQz.png?alt=media&token=8f895f65-b871-4b36-98e1-6fdf44df2dfd)
    - roam research如何与[[Obsidian]]同步？#[[软件联动]]#[[自创]]
        - 我自己也已经通过快捷方式可以让二者同步，也并不复杂，有空的时候再看看别人介绍的这个方法，好像[[github]]确实可以帮助完成很多事情。
        - Automatic RoamResearch backupVia[MatthieuBizien/roam-to-git: Automatic RoamResearch backup to Git](https://github.com/MatthieuBizien/roam-to-git) [[20211230]] 下午10:52
    - 如何用roam research看中观图景？
        - 其实我用obsidian就可以实现查看中观图景，因为obsidian的graph图呈现方式比roam research要好得多。好像[[王树义]]老师的方法也就是通过obsidian来优化的。最后好像也是通过[[github]]来同步。我目前的方法只能实现从roam research到obsidian的单项同步，如果能够实现双向同步就完美了。以下方法也只能实现单项同步，目前来看，我自己想到的把roam research和[[Obsidian]]联动起来的方法最好。[[软件联动]]
    - 怎么修改roam research导出的文件的格式？
        - https://roam-tools.ryanguill.com/?这个网站可以实现一些修改。
    - telegram发送内容到roam reseaerch。Telegram Bot
- 如何取消roam research左边栏？
    - 隐藏以后每次鼠标划过都会弹出来，看着很闹人。
    - 我以前用css修改过，但是没有保存经验，现在不会弄了。
    - 在群里问，有人告诉我方法了。非常好。
    - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FPdXPY9obGs.png?alt=media&token=bbe91f32-d2aa-4fe3-bb28-09ee17f80368)
- [[间隔记忆]]
    - roam research的内容转换成为[[Anki]]？
        - 学习骇客制作了一个工具，可以把按照一定格式组织起来的roam research内容批量生成卡片。我使用过，但是它制作的是问题-答案这种形式的卡片。我最近喜欢制作close形式的卡片，觉得更适合我。
    - 目前roam research的插件也可以使用了，具体可以参考以下网页
        - https://roamstack.com/kb/extensions/roam-sr/#installing-roam-sr
