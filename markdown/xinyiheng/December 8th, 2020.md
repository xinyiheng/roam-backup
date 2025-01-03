- [[Python]]
- #问题
    - {{[[DONE]]}}knowledgebase builder快捷确认和缩放文本@评论:不要追求完美。基本能用了。
- 画家与黑客#[[读书笔记]]
    - O'Reilly Media, Inc.介绍
      为了满足读者对网络和软件技术知识的迫切需求，世界著名计算机图书出版机构O'Reilly Media, Inc.授权人民邮电出版社，翻译出版一批该公司久负盛名的英文经典技术专著。
      O'Reilly Media, Inc.是世界上在 Unix、X、Internet 和其他开放系统图书领域具有领导地位的出版公司，同时也是联机出版的先锋。
      从最畅销的The Whole Internet User's Guide & Catalog
      （被纽约公共图书馆评为20世纪最重要的50本书之一）到最早的Internet门户和商业网站GNN，再到第一个桌面PC的Web服务器软件WebSite，O'Reilly Media,Inc.一直处于Internet发展的最前沿。
      许多书店的反馈表明，O'Reilly Media, Inc.是最稳定的计算机图书出版商——每一本书都一版再版
      -via[黑客与画家 - 得到APP](https://www.dedao.cn/reader?id=exGM6Evn5byxq2PnXBz71AjZaol6R8WJDawOKpGkd4gmMLEJrYNQe9VvD8P4jLkK)
    - 为什么说编程语言是设计而不是研究？
        - 如果把创造一种编程语言看成是设计问题，而不是科研方向，那么有何不同？
          最大的不同在于你会更多地考虑用户。设计的时候，一开始总是问：我为谁设计？他们需要什么？比如，优秀的建筑师不会先设计，然后强迫用户接受，而是先研究最终用户的需求，然后做出用户需要的设计。
    - 用户需求和用户要求有何不同？
      
        - 注意，我说的是“用户需要的设计”，而不是“用户要求的设计”。我不想让读者产生一种印象，认为设计师就像厨师一样，顾客点什么菜就一模一样做出来。艺术的各个领域有着巨大的差别，但是我觉得任何一个领域的最佳作品都不可能由对用户言听计从的人做出来。
          -via[黑客与画家 - 得到APP](https://www.dedao.cn/reader?id=exGM6Evn5byxq2PnXBz71AjZaol6R8WJDawOKpGkd4gmMLEJrYNQe9VvD8P4jLkK)
    - 怎样给用户画像才是合适的？
        - 如果目标用户群体涵盖了设计师本人，那么最有可能诞生优秀设计。如果目标用户与你本人差别很大，你往往会假定目标用户的需求比你本人的需求更简单，而不是更复杂。低估用户（即使出于善意）一般来说总是会让设计师出错。
          -via[黑客与画家 - 得到APP](https://www.dedao.cn/reader?id=exGM6Evn5byxq2PnXBz71AjZaol6R8WJDawOKpGkd4gmMLEJrYNQe9VvD8P4jLkK)
    - 什么是静态类型语言？什么是交互式顶层解释器？
        - 开发软件的时候，一个“交互式顶层解释器”（interactive toplevel）会带来巨大的优势。在Lisp语言中，这种解释器就叫做“读取—求值—打印”循环（read-eval-print loop）。有了这个解释器后，语言的设计就会受到巨大影响。静态类型语言不适合部署这样的解释器，因为静态类型语言要求在使用变量前先声明类型，这对于“交互式顶层解释器”行不通。当你在解释器中输入表达式，然后对变量x
          进行赋值，接着再对x
          做进一步处理时，你只想尽快看到结果，肯定不想很麻烦地先声明x
          的类型。你也许不同意“交互式顶层解释器”为软件开发带来便利的说法，但是如果你接受它，同意易于使用的编程语言必须有一个这样的解释器，那么强制声明变量类型的做法就是与这个解释器不兼容，因此结论就是所有的静态类型语言都不易于编程。
          -via[黑客与画家 - 得到APP](https://www.dedao.cn/reader?id=exGM6Evn5byxq2PnXBz71AjZaol6R8WJDawOKpGkd4gmMLEJrYNQe9VvD8P4jLkK)
    - 怎样才能写出平易近人的文章？
        - 奥斯汀的故事和白居易有些类似#[[写作]]
        - 19世纪英国作家简 · 奥斯汀的小说为何如此出色？一个原因就是她把自己的作品大声读给家人听，所以她就不会陷入孤芳自赏难以自拔的境地，不会长篇累牍地赞叹自然风光，也不会滔滔不绝地宣扬自己的人生哲学。（事实上，简 · 奥斯汀还是在小说里宣扬了自己的人生哲学，不过她把它编进故事之中，而不是直接像贴标签那样讲出来。）你可以随便找一本平庸的“文学”读物，想象一下把它当作自己的作品读给朋友们听，这样会让你真切地感受到那些“文学”读物高高在上的视角，读者必须承受所有沉重的负担才能阅读这些作品。
          -via[黑客与画家 - 得到APP](https://www.dedao.cn/reader?id=exGM6Evn5byxq2PnXBz71AjZaol6R8WJDawOKpGkd4gmMLEJrYNQe9VvD8P4jLkK)
    - 软件开发的两种思路：“弱即是强”和“万福玛利亚”
        - “弱即是强”指的是一种软件传播的模式，由Common Lisp专家理查德 · 加布里埃尔（Richard P. Gabriel）于1991年在Lisp: GoodNews, Bad News, How to WinBig（http://www.dreamsongs.com/WIB.html
          ）一文中首先提出。它的含义非常广泛，涉及软件设计思想的各个方面，其中的一个重要结论就是软件功能的增加并不必然带来质量的提高。有时候，更少的功能（“弱”）反而是更好的选择（“强”），因为这会使得软件的可用性提高。相比那些体积庞大、功能全面、较难上手的软件，一种功能有限但易于使用的软件可能对用户有更大的吸引力。加布里埃尔本人经常举Unix和C语言的例子，Unix和C在设计上考虑了实际环境，放弃了一些功能，但是保证了简单性，这使得它们最终在竞争中胜出，成为主流操作系统和编程语言。——译者注
          -via[黑客与画家 - 得到APP](https://www.dedao.cn/reader?id=exGM6Evn5byxq2PnXBz71AjZaol6R8WJDawOKpGkd4gmMLEJrYNQe9VvD8P4jLkK)
        - 还有另一种软件设计思想，也许可以被称为“万福玛丽亚”模式。它不要求尽快拿出原型，然后再逐步优化，它的观点是你应该等到完整的成品出来以后再一下子隆重地推向市场，就像圣母玛丽亚降临一样，哪怕整个过程漫长得像橄榄球运动员长途奔袭、达阵得分也没有关系。在互联网泡沫时期，无数创业公司因为相信了这种模式而自毁前程。我还没听说过有人采用这种模式而获得成功。
          -via[黑客与画家 - 得到APP](https://www.dedao.cn/reader?id=exGM6Evn5byxq2PnXBz71AjZaol6R8WJDawOKpGkd4gmMLEJrYNQe9VvD8P4jLkK)
        - 绘画为何也揭示了弱即是强的道理？画画的时候先勾勒出线条，这不会制约创造力，反而会成为不断完善的画作质量的支撑要素。软件设计的原理也是这样，原型可以修改，但是不用总是另起炉灶。
        - 有些接近“迭代”和尽快把车开出车库的说法。用我的话就是“丑媳妇总要见公婆”
    - **士气是设计的关键因素**。令我吃惊的是，大家很少提到这一点。我的一位美术启蒙老师告诉我：如果你觉得画某样东西很乏味，那么你画出来的东西就会真的很乏味。比如，假设你必须画一幢建筑物，你决定从每一块砖头开始画起。你觉得自己可以坚持下去，但是画到一半的时候突然感到很厌倦，于是你就不再认真观察每块砖头并画出它们各自不同的特点，而是以一种机械重复的方式草草地把砖头画完了事。这样一来，你的作品效果就很差，甚至还不如一开始就不采用写实手法，只是若隐若现地暗示砖头的存在。
      -via[黑客与画家 - 得到APP](https://www.dedao.cn/reader?id=exGM6Evn5byxq2PnXBz71AjZaol6R8WJDawOKpGkd4gmMLEJrYNQe9VvD8P4jLkK)
    - 这一点我也很赞同。如果你不相信或者喜欢自己正在做的事情，好像作品就会缺乏生命力。
    - 一种编程语言流行与否很大程度上也在于宣传。
        - 大家都觉得Java一定有过人之处，因为它是一种很酷的新兴编程语言。但是真的如此吗？如果你站在远处观察编程语言的世界，似乎Java就是最新的东西。（如果你站得足够远，那么你看到的所有东西就是Sun公司出钱制作的大型霓虹广告牌。）但是，如果你靠近观察这个世界，就会发现不同的人对“酷”的理解是不一样的。在黑客圈子里，Perl被公认比Java酷得多。黑客社区网站Slashdot就是用Perl开发的。我估计你不可能看到黑客愿意使用Java的JSP技术开发网站。可是，还有一种更新的语言叫做Python，它的使用者往往看不起Perl。另一些人则认为Ruby语言是取代Python的最佳选择。
          -via[黑客与画家 - 得到APP](https://www.dedao.cn/reader?id=exGM6Evn5byxq2PnXBz71AjZaol6R8WJDawOKpGkd4gmMLEJrYNQe9VvD8P4jLkK)
    - 为什么1958年诞生的Lisp语言比现在流行的语言更先进？
        - 当你按照Java、Perl、Python、Ruby这样的顺序观察这些语言，你会发现一个有趣的结果。至少，如果你是一个Lisp黑客，你就看得出来，排在越后面的语言越像Lisp。Python语言模仿Lisp，甚至把许多Lisp黑客认为属于设计错误的功能也一起模仿了。至于Ruby语言，如果回到1975年，你声称它是一种有着自己句法的Lisp方言，没有人会提出反对意见。编程语言现在的发展不过刚刚赶上1958年Lisp语言的水平。
          -via[黑客与画家 - 得到APP](https://www.dedao.cn/reader?id=exGM6Evn5byxq2PnXBz71AjZaol6R8WJDawOKpGkd4gmMLEJrYNQe9VvD8P4jLkK)
        - 让我告诉你原因。这是因为设计者本来没打算把Lisp设计成编程语言，至少不是我们现在意义上的编程语言。我们今天所说的编程语言指的是用来告诉计算机怎么做的一种工具。麦卡锡最后确实有意开发这种意义上的编程语言，但是实际上他做出来的Lisp却是完全不同的一种东西，语言的基础是他的一种理论演算，他想用更简洁的方式定义图灵机。正如他后来所说
          -via[黑客与画家 - 得到APP](https://www.dedao.cn/reader?id=exGM6Evn5byxq2PnXBz71AjZaol6R8WJDawOKpGkd4gmMLEJrYNQe9VvD8P4jLkK)
        - 1958年年底，麦卡锡的一个学生史蒂夫 · 拉塞尔看到了eval函数的定义，意识到如果把它翻译成机器语言，就可以把Lisp解释器做出来。
          Steve Russell，也是历史上第一个电脑游戏的作者，1962年他写了《太空大战》（Spacewar）。#[[轶事]]
          -via[黑客与画家 - 得到APP](https://www.dedao.cn/reader?id=exGM6Evn5byxq2PnXBz71AjZaol6R8WJDawOKpGkd4gmMLEJrYNQe9VvD8P4jLkK)
        - 由此也就得出了20世纪50年代的编程语言到现在还没有过时的原因。简单说，因为**这种语言本质上不是一种技术，而是数学**。数学是不会过时的。你不应该把Lisp语言与50年代的硬件联系在一起，而是应该把它与快速排序（Quicksort）算法进行类比。这种算法是1960年提出的，至今仍然是最快的通用排序方法。
          -via[黑客与画家 - 得到APP](https://www.dedao.cn/reader?id=exGM6Evn5byxq2PnXBz71AjZaol6R8WJDawOKpGkd4gmMLEJrYNQe9VvD8P4jLkK)
    - 编程语言的两种发展方向的代表是什么？
        - Lisp和Fortran代表了编程语言发展的两大方向。前者的基础是数学，后者的基础是硬件架构。从那时起，这两大方向一直在互相靠拢。Lisp语言刚设计出来的时候就很强大，接下来的二十年它提高了运行速度。而那些所谓的主流语言把更快的运行速度作为设计的出发点，然后再用四十多年的时间一步步变得更强大。直到今天，最高级的主流语言也只是刚刚接近Lisp的水平。虽然已经很接近了，但还是没有Lisp那样强大。
          -via[黑客与画家 - 得到APP](https://www.dedao.cn/reader?id=exGM6Evn5byxq2PnXBz71AjZaol6R8WJDawOKpGkd4gmMLEJrYNQe9VvD8P4jLkK)
    - 为什么这么强大的编程语言没有流行起来？未来趋势怎样？
        - 使用一种不常见的语言会出现的问题我想到了三个：你的程序可能无法很好地与使用其他语言写的程序协同工作；你可能找不到很多函数库；你可能不容易雇到程序员。
          -via[黑客与画家 - 得到APP](https://www.dedao.cn/reader?id=exGM6Evn5byxq2PnXBz71AjZaol6R8WJDawOKpGkd4gmMLEJrYNQe9VvD8P4jLkK)
        - 未来得到应用的概率更大了，因为可以把软件安置在服务器端，从而不用受制于用户使用的终端的操作系统。
    - 怎样衡量一种编程语言高级与否？
        - 衡量语言的编程能力的最简单方法可能就是看代码数量。所谓高级语言，就是能够提供更强大抽象能力的语言，从某种意义上，就像能够提供更大的砖头，所以砌墙的时候用到的砖头数量就变少了。因此，语言的编程能力越强大，写出来的程序就越短（当然不是指字符数量，而是指独立的语法单位）。
          -via[黑客与画家 - 得到APP](https://www.dedao.cn/reader?id=exGM6Evn5byxq2PnXBz71AjZaol6R8WJDawOKpGkd4gmMLEJrYNQe9VvD8P4jLkK)
        - 代码的数量很重要，因为开发一个程序所耗费的时间主要取决于程序的长度。对于同一个软件，如果用一种语言写出来的代码比用另一种语言长三倍，这意味着你开发它耗费的时间也会多三倍。而且即使多雇人手，也无助于缩短开发时间，因为当团队规模超过某个门槛时，再增加人手只会带来净损失。Fred Brooks在他的名著《人月神话》中描述了这种现象，我的所见所闻印证了他的说法。
          -via[黑客与画家 - 得到APP](https://www.dedao.cn/reader?id=exGM6Evn5byxq2PnXBz71AjZaol6R8WJDawOKpGkd4gmMLEJrYNQe9VvD8P4jLkK)
    - 为什么不应该遵循”业界最佳标准“？
        - 大型组织内部，有一个专门的术语描述这种跟随大多数人的选择的做法，叫做“业界最佳实践”。这个词出现的原因其实就是为了让你的经理可以推卸责任。既然我选择的是“业界最佳实践”，如果不成功，项目失败了，那么你也无法指责我，因为做出选择的人不是我，而是整个“业界”。
          -via[黑客与画家 - 得到APP](https://www.dedao.cn/reader?id=exGM6Evn5byxq2PnXBz71AjZaol6R8WJDawOKpGkd4gmMLEJrYNQe9VvD8P4jLkK)
- obsidian的关系图谱要怎么用
  -via[obsidian的关系图谱要怎么用 - 知乎](https://zhuanlan.zhihu.com/p/237351391)
    - 有一款叫思源笔记的，可在某个笔记内鼠标点击不同被链接的内容，在笔记不变的情况下图谱在节点与节点间动画切换。[[Obsidian]] 0.8.13版只能做到点击图谱或某个被链接标题，同时切换。
      -via[Obsidian]]的关系图谱要怎么用 - 知乎](https://zhuanlan.zhihu.com/p/237351391)
    - 用小关系图读书收集（小关系图谱的拓展运用）
      因软件bug此节待开发者修复后再更新···
      实际就是固定住图谱使图谱不变，让某个节点为中心主题，围绕着这个中心主题来进行读书、收集和笔记。（目前0.9.0版还存在这个缺陷）
      -via[obsidian的关系图谱要怎么用 - 知乎](https://zhuanlan.zhihu.com/p/237351391)
    - 你应该把每个单独的笔记看作一个脑图的节点，这样你就会有一个全局的思维、全局视野，对你的思维和智商都是有利的，这样自然而然的你的图谱也变得可用性很高，因为它会是一个可供观察有结构有体系的一个”树网合一“的图谱。
      -via[obsidian的关系图谱要怎么用 - 知乎](https://zhuanlan.zhihu.com/p/237351391)
    - 每个单独笔记的标题对应一个图谱的节点，每个节点应该就是一个独立的意义的”知识块“，这样也符合zk笔记的方法，也便于你后期直接通过图谱就看到你想要的东西。而不是一般笔记下（一个图谱节点下）什么内容都冗长的记录在里边，这样一来你通过图谱就无法看出来这个节点”到底是怎么回事“，图谱就是失去了意义。
      -via[obsidian的关系图谱要怎么用 - 知乎](https://zhuanlan.zhihu.com/p/237351391)
    - 关于树状结构的建立与观察
      一般的树状结构的建立，在`[[A]]`笔记内写入`[[k]]`，就建立了k是a的子项的关系，这是一种最简单的树状结构的建立，书写时建立树状结构最简单的办法。更具体的方式就是接在`[[笔记a]]`中写入`[[k]]、[[a-1]]···`，`[[a-1]]`中又丢入`[[xxx]]`，这样也能直接建立一个强大的树状体系或网状体系。
      -via[obsidian的关系图谱要怎么用 - 知乎](https://zhuanlan.zhihu.com/p/237351391)
    - 在建立笔记时你可以利用前缀、后缀、序号+当前内容标题的方式很方便的建立树状结构，比如`[[大头儿子的家]]、[[大头儿子的家-01-大头儿子]]、[[大头儿子的家-02-小头爸爸]],[[小头爸爸-钱包]]`。前缀、后缀、序号+当前内容标题的方式就可以让你可以轻松溯源，找到结构，要注意的是在上一级已经和上上一级已经挂钩的情况下，这级一般就无需再把上上一级作为前缀，这样有三个好处，一个就是目前这级也是一个独立的知识块方便被引用，标题简短易于在图谱中查看（直接能看出父子关系脑图结构），利于专注在当下的主题发散不受更大类别的框架限制。
      -via[obsidian的关系图谱要怎么用 - 知乎](https://zhuanlan.zhihu.com/p/237351391)
    - 为什么以及如何对一些节点减肥？
        - 通过obsidian的图谱观察，你会发现某些节点太肥了，某些节点内承载的链接量（知识量）实在太密集导致”肥胖“，这样的节点是过于囊肿的节点，一个节点内容包含了太多的意义，不利于思考、阅读（因为人脑前额区算力有限，内容太多太杂不利于专注学习和阅读会产生混乱）和被引用，这时就需要减肥，可以把这个节点年的内容先用#小标题归类，内容形成一个相对独立的知识块后就可以把小标题转化为一个新的`[[新的笔记]]`就可以完成减肥，这样还有几个好处，你只利用图谱观察时也能看见很多本来”隐藏“了的重要内容，因为你对内容进行了再次归纳你些知识的把握就更为明确，思路更加清晰，不会再混乱。
          -via[obsidian的关系图谱要怎么用 - 知乎](https://zhuanlan.zhihu.com/p/237351391)
- 巧用Obsidian把“思维导图”变成“双向链思维导图”
  -via[巧用Obsidian把“思维导图”变成“双向链思维导图” - 知乎](https://zhuanlan.zhihu.com/p/269279110)
