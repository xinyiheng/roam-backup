- 有很多mac中目前使用的打开软件的#[[快捷方式]]
- triger里选择palette也有好处，我之前很少使用这种功能。
- mac上的大部分常用的[[快捷方式]]都是通过这个软件创建的。
- 这个软件可以帮助实现自动化。我快速打开一些网站的功能就是通过这一软件实现的。比如command+b打开toby。
- Folder Trigger：这个触发器会关注某个特定文件夹，当这个文件夹添加了新文件，移除了文件，添加或移除了文件时，触发。 [sspai.com](https://sspai.com/post/36442)
- 
- 主要用来快速启动软件。设置键盘快捷键比用afred还快，并且启动界面更好。
- 现在才知道[[keyboard maestro]]设置触发[[快捷方式]]的时候原来只使用字母也可以，不用非加上command、alt之类的功能键，这样，我设置快捷方式的空间又打了很多，不会冲突了。比如，我把印象笔记的启动方式从command+y变成了“YX”(小写的)，我现在没有办法直接连着打出这两个字母了，因为会直接启动印象笔记而不是显示这两个字母。解决办法就是分开输入，先打y然后再打出x。#[[进步]]
- 现在可以设置一些简单的宏来合并几个重复的动作。
- [[Automator]]
- #[[参考资料]]
    - Official Keyboard Maestro WikiVia[Home Page [Keyboard Maestro Wiki[[[[]](]]]]https://wiki.keyboardmaestro.com/Home_Page)[[20210106]] 下午5:15 
    - [Keyboard Maestro 入门指南 - 少数派](https://sspai.com/post/36442) 
    - [Keyboard Maestro 和它的 Macro 们 | 2016与我的数字生活 - 少数派](https://sspai.com/post/36707) 
    - [用 Keyboard Maestro 实现窗口排列管理 - 少数派](https://sspai.com/post/55908)
    - 用 Keyboard Maestro 做一个文本格式转换工具箱keyboard maestro
    - 
-via[用 Keyboard Maestro 做一个文本格式转换工具箱 - 少数派](https://sspai.com/post/56851)
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
via[Regular Expressions [Keyboard Maestro Wiki[[[[]](]]]]https://wiki.keyboardmaestro.com/Regular_Expressions?s[]=regular)
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
