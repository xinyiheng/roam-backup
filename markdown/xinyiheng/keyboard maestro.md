- 我是如何使用keyboard maestro从mac电脑不同的位置向[[Roam Research]]搬运内容并自动生成链接的？@评论:受到[[john15263]]设计的little john的启发。
    - 实现了终极完美的阅读笔记功能，可以在浏览器阅读，把选中的内容直接复制到
      [[Roam Research]]中，然后还带着url链接。主要使用的软件是[[keyboard maestro]]，只使用了一点简单的[[Applescript]]脚本。#[[软件联动]]用[[BetterTouchToo]]设置了在[[触控板]]双指向左滑动就可以启动的#[[快捷方式]]然后还带着url链接。最困难的部分是怎样在roam research当中新建一个条目，最初的想法是用keyboard maestro当中的find image and click 的功能，这样准确率还可以，但是很难提高到100%。我后来想到可以查看roam resaerch当中的快捷键，发现有一个快捷方式可以快速跳转到最新的一个条目，一下豁然开朗。可以用模拟某个软件快捷按键的方式来实现很多功能。
      #[[阅读管理]]
        - 用法示例
            - 在[[得到电子书]]app网页版阅读书籍
                - 生活中有很多小道理，你如果不满足于一次就事论事，能把这个道理给提炼出来，取个名字，就更容易推而广之，成为一个有力的工具。比如我一说“唇亡齿寒”、“酸葡萄”，你马上就知道是什么意思，这些名词相当于是把思维套路给封装起来，方便使用。#[[常识]]
                - via[能用愚蠢解释的，就不要用恶意 - 得到APP](https://www.dedao.cn/article/Q8dpgOa54NZMVzmmZNKByzxkwYm2Rl)
                    - 例子
                        - 研究所领导徐治功给全所发了个邮件，要求所有研究人员在一周之内上报自己这一年来的工作进展。大家都知道这个报告会影响到明年的科研经费，都非常认真地准备。结果一周过后，唯独秦奋没有交报告。徐治功说你怎么回事？秦奋说哎呀我忘了！
                        - 又过了三天，徐治功又找秦奋，但是秦奋还是没写。他居然说又忘了。徐治功非常生气，说秦奋你是在侮辱我的智商吗？你知不知道我拿到你们的报告之后还要综合形成全所的报告，现在我的时间都不够了！啊我明白了，上次评职称没让你过，你报复我是不是？
                        - 秦奋说领导我冤枉啊！你知不知道有个法则，叫“汉隆剃刀”。
                    - “汉隆剃刀（Hanlon's razor）”大约是 1990 年一个叫汉隆的不著名的美国人正式提出来的，但是这个道理前人多有提及。你可以把汉隆剃刀理解成著名的“奥卡姆剃刀”的一个特殊情况。简单地说，它的意思是 ——
                        - 「能解释为愚蠢的，就不要解释为恶意。」
                        - 举个例子。比如你今天晚上有个重要的报告要在家里写，你正忙得焦头烂额。你三岁的儿子，平时不怎么找你，今天却非得缠着你，然后还打碎了一个碗。那你说他是故意挑这个时候跟你作对吗？
                        - 当然不是。他根本不理解你要写报告，他只是碰巧今天想找你玩而已。
                    - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2F32oy32xAHh.png?alt=media&token=e72996f1-6ee3-4956-a669-a030675e1a61)
            - 在[[微信读书]]app网页版阅读
                - via[麦肯锡职场训练营：菜鸟晋升职场精英（套装共9册）-赤羽雄二 大岛祥誉 安宅和人 高杉尚孝等-微信读书](https://weread.qq.com/web/reader/277327d071916d4e277776eke4d32d5015e4da3b7fbb1fa)
                    - 前 言能有所成长真是太美妙了对我们而言，最开心的事是什么呢？如果在工作中取得了好成绩，想必会很开心吧。在此基础上，个人生活也过得十分充实，应该就会更加开心了。但是，以上的情况也要视环境和面对的人而定，我们无法百分之百掌控局面。有时候，是否会取得成功，与自己付出的努力并无关系
            - 在普通网页阅读
                - via[给所有人用的配色 App，你手机里的专属「设计师」：色采 - 少数派](https://sspai.com/post/63476)
                    - 即使你没有意识到，但从你拿起新手机设置壁纸时开始，就和大部分人一样渴望令它变得更独属于自己，更加符合自己的审美。
                    - 这个拿在手上已经离不开的小方块更像是我们的「第二个家」。无论是简单地换壳贴纸、设置壁纸换个图标，还是应用主题商店琳琅满目中一见钟情的主题，甚至高级的自定义美化玩法，都像装修爱巢般使手机进一步迎合自我个性，让我们的生活更加缤纷。
            - 在[[印象笔记]]网页版阅读
                - 这样的好处是可以永久保留网页。对于比较重要的网页可以取用这种方式。
            - 现在还可以在[[Marginnote]]阅读
- 有很多mac中目前使用的打开软件的#[[快捷方式]]
- 该软件使用的正则表达式为ICU正则表达式 [ICU 正则表达式 - IBM 文档](https://www.ibm.com/docs/zh/iad/7.2.1?topic=configuration-icu-regular-expressions)
- triger里选择palette也有好处，我之前很少使用这种功能。
- ### 如何把双击control键作为触发条件？
    - 为了方便唤起alfred，我把alfred搜索的触发键从双击control键转换为了 control+option+command+h，但是我又不像放弃原来的触发体验，所以用keiboard maestrol设置了一个快捷键，用双击contro触发control+option+command+h 🗒@评论:缺点是只能在外接键盘上使用，无法在内置键盘上使用。
    - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FdQRcjJcHTC.png?alt=media&token=8f8614ae-a156-41ef-a701-61bf418bd0dc)
    - [Double Tap Control - Macro Library - Keyboard Maestro Discourse](https://forum.keyboardmaestro.com/t/double-tap-control/202)
- mac上的大部分常用的[[快捷方式]]都是通过这个软件创建的。
- 这个软件可以帮助实现自动化。我快速打开一些网站的功能就是通过这一软件实现的。比如command+b打开toby。
- Folder Trigger：这个触发器会关注某个特定文件夹，当这个文件夹添加了新文件，移除了文件，添加或移除了文件时，触发。 [sspai.com](https://sspai.com/post/36442)
- 主要用来快速启动软件。设置键盘快捷键比用afred还快，并且启动界面更好。
- 现在才知道[[keyboard maestro]]设置触发[[快捷方式]]的时候原来只使用字母也可以，不用非加上command、alt之类的功能键，这样，我设置快捷方式的空间又打了很多，不会冲突了。比如，我把印象笔记的启动方式从command+y变成了“YX”(小写的)，我现在没有办法直接连着打出这两个字母了，因为会直接启动印象笔记而不是显示这两个字母。解决办法就是分开输入，先打y然后再打出x。#[[进步]]
- 现在可以设置一些简单的宏来合并几个重复的动作。
- https://dida365.com/webapp/#p/inbox/tasks/63aa2eee4b841102ba86d7b9
- [[Automator]]
- ### 如何快速出'#[[]]'
    - 在roam中打出这个符号需要用到shift+3 这两个键，我以前使用模拟按键的时候因为要使用到shift这个键，所以经常会让输入法在中英文之间切换。后来我想到可以直接把这个符号当作文字来输入就可以了。但是需要让光标在两个方括号中间，我在网上查看用%|%就可以代替光标的位置。
    - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FBLBjBN_XsV.png?alt=media&token=47d7bb7c-a1b6-4d61-8240-4edf3ac89b6e)
    - [Is there a way to have KM place the cursor within a pasted object?](https://forum.keyboardmaestro.com/t/is-there-a-way-to-have-km-place-the-cursor-within-a-pasted-object/9365)
- #[[参考资料]]
    - Official Keyboard Maestro WikiVia[Home Page [Keyboard Maestro Wiki[[]](]]https://wiki.keyboardmaestro.com/Home_Page)[[20210106]] 下午5:15 
    - [Keyboard Maestro 入门指南 - 少数派](https://sspai.com/post/36442) 
    - [Keyboard Maestro 和它的 Macro 们 | 2016与我的数字生活 - 少数派](https://sspai.com/post/36707) 
    - [用 Keyboard Maestro 实现窗口排列管理 - 少数派](https://sspai.com/post/55908)
    - 用 Keyboard Maestro 做一个文本格式转换工具箱keyboard maestro
    - via[用 Keyboard Maestro 做一个文本格式转换工具箱 - 少数派](https://sspai.com/post/56851)
    - 以 Word 为例，让你更快入门 Keyboard Maestro
      -via[以 Word 为例，让你更快入门 Keyboard Maestro - 少数派](https://sspai.com/post/44091)
    - 用 Keyboard Maestro 实现剪贴板顺序粘贴
      -via[用 Keyboard Maestro 实现剪贴板顺序粘贴 - 少数派](https://sspai.com/post/56648)
        - Keyboard Maestro 中的 Palette（浮窗）就可以作为顺序粘贴模式的开关。我们可以把动作放在一个专门的组（Group）里面，只有先呼出包含这组动作的 Palette，才会激活顺序拷贝和粘贴的动作，不影响日常使用 ⌘Command-C 和 ⌘Command-V。
          具体设置是，两个动作放在同一个组里，组设置为「Shows/hides a palette when: The hot key 你喜欢的快捷键 is pressed」，并且勾选「Display when toggled」，这样每次复制/粘贴后 Palette 不至于自动消失，你可以放心地连续拷贝数据。
          via[用 Keyboard Maestro 实现剪贴板顺序粘贴 - 少数派](https://sspai.com/post/56648)
          [[20201211]] 上午7:07
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FSuWZKXmP8Y.png?alt=media&token=2ee2a7ae-174b-44ac-b7ad-8018246a3323)
        - 在追加文本部分，我们用到了两个 Keyboard Maestro 内置变量，它们是 %SystemClipboard%（系统剪贴板）和 %LineFeed%（换行符号）。自己制作或编辑动作时，在任何支持使用变量的地方（几乎所有文本框）都可以通过「Insert Token」来插入变量。
          via[用 Keyboard Maestro 实现剪贴板顺序粘贴 - 少数派](https://sspai.com/post/56648)
          [[20201211]] 上午7:13
        - 我已经从github下载了别人设置好的macro，还没有开始使用。
        - 到此为止，剩下的事情就是在变量中尚有内容时，如何解决依次取用和删除用过的内容两大问题。本文动作通过一段 AppleScript 脚本和一条正则表达式分别解决了两个难点：
          用 AppleScript 提取第一行：提取第一行文本并且拷贝到剪贴板。AppleScript 也有删除文本的功能，但是它对于换行符号的处理不佳，会造成 Keyboard Maestro 无法对 AppleScript 处理过的文本正确分行，所以我们用下面的方法完成文本删除。
          用正则表达式删除第一行：删除的要求是只删用过的第一行，这个需求可以通过表达式 ^.*[\n\r] 完成，它表示「从文本开头到第一次换行」，也就是第一行，把这个表达式表示的内容替换成空白即是删除。这正则技巧来自 Keyboard Maestro 论坛上的一则讨论（Remove the top line of a text file or variable）。
          via[用 Keyboard Maestro 实现剪贴板顺序粘贴 - 少数派](https://sspai.com/post/56648)
          [[20201211]] 上午7:23
    - 在Keyboard Maestro中替换空行
      via[在Keyboard Maestro中替换空行 - 简书](https://www.jianshu.com/p/b25bdde6e5c6)
      [[20201211]] 上午9:03
    - keybaord maestro自带的[[正则表达式]]说明
        - Regular Expressions (RegEx)
          via[Regular Expressions -Keyboard Maestro Wik](https://wiki.keyboardmaestro.com/Regular_Expressions?s[]=regular)
          [[20201211]] 上午9:06
    - 用 Keyboard Maestro 托拽整理文件
      -via[用 Keyboard Maestro 托拽整理文件 - 少数派](https://sspai.com/post/44429)
    - 帮我打造 OmniFocus 工作流的得力助手：「模板脚本」的使用分享 | 2016 与我的数字生活
      -via[帮我打造 OmniFocus 工作流的得力助手：「模板脚本」的使用分享 | 2016 与我的数字生活 - 少数派](https://sspai.com/post/36927)
    - 如何更方便地启用 macOS 菜单栏功能
      -via[如何更方便地启用 macOS 菜单栏功能 - 少数派](https://sspai.com/post/46169)
    - 用 Keyboard Maestro 自动开启「生活模式」
      -via[用 Keyboard Maestro 自动开启「生活模式」 - 少数派](https://sspai.com/post/42322)
    - 如何用语音控制电脑
      -via[如何用语音控制电脑 - 少数派](https://sspai.com/post/45630)
    - Automator 简单介绍及入门玩法 | Matrix 精选
      -via[Automator 简单介绍及入门玩法 | Matrix 精选 - 少数派](https://sspai.com/post/36667)
    - keyboard maestro
        - 🦩[Latest topics - Keyboard Maestro Discourse](https://forum.keyboardmaestro.com/latest) @评论:官方论坛
        - [Keyboard Maestro 9.2: Work Faster with Macros for macOS](https://www.keyboardmaestro.com/main/#Pricing)
        - [Latest Tips & Tutorials topics - Keyboard Maestro Discourse](https://forum.keyboardmaestro.com/c/tips/14)
        - [MacSparky](https://www.macsparky.com/)
        - [Home Page [Keyboard Maestro Wiki](https://wiki.keyboardmaestro.com/doku.php)
        - [manual:Features [Keyboard Maestro Wiki](https://wiki.keyboardmaestro.com/manual/Features)
        - [User Manual [Keyboard Maestro Wiki](https://wiki.keyboardmaestro.com/User_Manual)[Double Tap Control - Macro Library - Keyboard Maestro Discourse](https://forum.keyboardmaestro.com/t/double-tap-control/202)
