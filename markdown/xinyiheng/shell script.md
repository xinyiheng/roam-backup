- shell script有哪些种类？
    - Shell 脚本（shell script），是一种为 shell 编写的脚本文件，一般文件后缀为 .sh。
    - shell scrip有不同的脚本语言，也对应着不同的脚本解释器。就像是不同的软件写的文件只能用对应的软件来读取。
    - 虽然脚本解释器不同，但是并不意味着换一种脚本语言就要更换一种软件。目前主流的shell应用程序都内置多种脚本解释器。比如，mac的终端既可以支持bash，又支持zch
    - [[文本编辑器]]和[[脚本解释器]]，以下指的既是脚本语言，又指其对应的脚本解释器
        - [[zsh]]目前，我的mac电脑终端默认的shell已经从bash编程了zsh，至于二者的区别我并不是很清楚，据说，zsh完美兼容bash，并且有比bash更强大的功能，用起来也比bash更优雅。
        - [[bash]] - 即 Bourne Again Shell。bash 是 Linux 标准默认的 shell。实际上 Bash 这个名称就是 __Bourne-again shell__ 的首字母缩略词，而 Bourne shell 从维基的定义中可以看出是 Bash 的前身，即另一个（有点过时的）命令行工具。
        - [[sh]] - 即 Bourne Shell。sh 是 Unix 标准默认的 shell。
        - [[csh]]
        - [[fish]]
        - [[fish]] - 智能和用户友好的命令行 shell。
          
        - [[xiki]] - 使 shell 控制台更友好，更强大。
          via[一篇文章让你彻底掌握 shell 语言 - 静默虚空 - 博客园](https://www.cnblogs.com/jingmoxukong/p/7867397.html#11-%E4%BB%80%E4%B9%88%E6%98%AF-shell)
          [[20201217]] 上午9:20
        - 如何指定脚本解释器？
          
            - 在 shell 脚本，#! 告诉系统其后路径所指定的程序即是解释此脚本文件的 Shell 解释器。#! 被称作[[shebang]]（也称为 Hashbang ）。
              所以，你应该会在 shell 中，见到诸如以下的注释：
              指定 sh 解释器
              #!/bin/sh
              指定 bash 解释器
              #!/bin/bash
              via[一篇文章让你彻底掌握 shell 语言 - 静默虚空 - 博客园](https://www.cnblogs.com/jingmoxukong/p/7867397.html#11-%E4%BB%80%E4%B9%88%E6%98%AF-shell)
              [[20201217]] 上午9:21
        - 任何在字符界面能启动的程序都可以在Python中使用管道对象
          （pipe object）来启动。管道对象代表一个正在运行的程序。
          via[像计算机科学家一样思考Python（第2版） - 得到APP](https://www.dedao.cn/reader?id=bBVDEXGGLn7eB51b8NjVRqDoQJPMk3aXaJWadYrXmAxE4Ov92lgzK6ZypxLqdQjp)
          [[20201218]] 下午5:54
- 使用shell script可以做什么？
    - 可以取代[[Finder]]或者资源管理器来管理文件。[[文件处理]]
        - 新建、删除文档
          
            - 在合适的目录下输入：
              
              $ touch sinan-talk.txt
              看一眼 Finder，或接着输入 ls 指令，是不是能看到一个名为“sinan-talk”的 txt 空白文档？用 touch 指令新建任意文档就是这么简单。
              
              删除一个文档可以：
              
              $ rm sinan-talk.txt
              rm 即为 remove 缩写。
              
              rm 还可以用来重命名文档，使用方法如下：
              
              $ rm old-name.txt new-name.txt
              rm 删除掉的文档或文件夹不会出现在垃圾桶中，小白请慎用。
              via[写给小白的第一份命令行工具Bash教程](https://sinantang.github.io/a%20developer%20guide%20for%20newbies%20-%20starting%20with%20python/2018/01/27/Bash-for-beginners/)
              [[20201225]] 下午5:07
        - 预览文档内容
          
            - 找一个内容的文档，在其目录下输入：
              
              $ less sinan-talk.md
              .md 是 Markdown 格式文档的扩展名。
              
              此时你会看到 Terminal 窗口变成了 sinan-talk.md 这个文档内容的预览窗口。这个功能是 less 实现的。
              
              退出预览点击 q 。
              
              除了文字文档外，还有很多文件类型都能直接在 Terminal 预览，比如音频文件（但需要多走一步安装其他类似 less 的小工具）。
              
              
              via[写给小白的第一份命令行工具Bash教程](https://sinantang.github.io/a%20developer%20guide%20for%20newbies%20-%20starting%20with%20python/2018/01/27/Bash-for-beginners/)
              [[20201225]] 下午5:08
        - 查看文档内容，合并文档
          
            - 查看文档内容除了用 less 指令外，还常用到 cat。cat 不会跳到预览界面，而会把文档内容直接返回。比如，
              
              $ cat sinan-talk.md
              ### 玩转命令行工具 Bash — 马上让你看起来像个资深程序员！
              ...
              除此之外，cat 还可以用来做简单拼接文档的工作。比如，
              
              $ cat f1.txt
              Programming is the most fun
              $ cat f2.txt
              when you can have your clothes on.
              $ cat f1.txt f2.txt > newfile.txt
              $ cat newfile.txt
              Programming is the most fun
              when you can have your clothes on.
              cat 本身是 concatenate（串联）的缩写，即“首尾相连接在一起”。
              
              这里涉及到 > 这个符号。虽然是半角大于号，但在 Bash 脚本中常可以把 > 看作用于指向的箭头。cat f1.txt f2.txt > newfile.txt 里 > 很形象地指向了一个保存拼接内容的文档名称。
              
              这里的 newfile.txt 既可以是先前不存在的文档（电脑会即时创建这个新文档）；也可以是已经存在的文档（但此步操作会覆盖掉文档中原有内容）。
              via[写给小白的第一份命令行工具Bash教程](https://sinantang.github.io/a%20developer%20guide%20for%20newbies%20-%20starting%20with%20python/2018/01/27/Bash-for-beginners/)
              [[20201225]] 下午5:08
        - 查看文档大小、长度、字数
          
            - 这个需求也非常常见。用 wc 这个小工具即可快速查看各种大小参数。
              
              wc 是 wordcount 缩写。
              
              wc [-options] [file] 这个指令可以配不同的选项（options, 也称 flags）。通过明确不同的选项，可以分别查看文档的字数、行数、字节数。具体如下：
              
              -c 字节数
              
              -l 行数
              
              -w 字数
              
              例如：
              
              $ wc -l blog-post-80.txt
              	366 blog-post-80.txt
              $ wc -w blog-post-80.txt
              	1772 blog-post-80.txt
              $ wc -c blog-post-80.txt
              	18857 blog-post-80.txt
              via[写给小白的第一份命令行工具Bash教程](https://sinantang.github.io/a%20developer%20guide%20for%20newbies%20-%20starting%20with%20python/2018/01/27/Bash-for-beginners/)
              [[20201225]] 下午5:08
        - 不想浏览长文档的全部内容
          
            - 在程序员的日常中常常需要处理很大的文档（成千上万行内容或更多），这种时候没有正常人会直接打开这个文档（因为太慢，或有些编辑器不支持，或太占用电脑的 working memory），也不便于在命令行直接浏览。此时有个只浏览前 N 行的小指令就非常方便了。
              
              这种情况下我们可以使用 head 指令。
              
              $ wc -l long-file.txt
              234124
              $ head -10 long-file.txt
              Programming today is a race between software engineers striving to build bigger and better idiot-proof programs, 
              and the universe trying to build bigger and better idiots. 
              So far, the universe is winning.
              ...
              head 紧跟的数字选项是你想查看的前 N 行内容。前 10 行即为 head -10.
              
              配上上面刚学到的 > ，head 还可以非常方便地选中文档前 N 行内容并单独保存到另一个新文档中。
              
              $ head -10 long-file.txt > short-file.txt
              这样就不用在文档之间跳来跳去地反复“复制粘贴”啦。
              
              
              via[写给小白的第一份命令行工具Bash教程](https://sinantang.github.io/a%20developer%20guide%20for%20newbies%20-%20starting%20with%20python/2018/01/27/Bash-for-beginners/)
              [[20201225]] 下午5:09
        - 用文本编辑器打开文档
          
            - 这个指令就很简单啦！如果我想用 Atom 或 SublimeText 这两个主流文本编辑器打开一个文档以便进一步编辑，可以这样：
              
              $ atom sinan-talk.md
              $ subl sinan-talk.md
              此时会跳出相应的应用界面。
              
              如果想一次性打开此目录下所有文档，可以用 . 表示：
              
              $ atom .
              （以上操作的前提是你已经下载安装了 Atom 或 SublimeText，否则请看第一篇）
              via[写给小白的第一份命令行工具Bash教程](https://sinantang.github.io/a%20developer%20guide%20for%20newbies%20-%20starting%20with%20python/2018/01/27/Bash-for-beginners/)
              [[20201225]] 下午5:09
        - 
- 如何使用shell script？
    - 常用的命令符号列表
        - 命令符	含义
          pwd	打印工作目录
          hostname	计算机网络运营商名称
          mkdir	创建目录
          cd	切换目录
          ls	列示目录
          rmdir	移除目录
          pushd	前往新目录地址
          popd	返回原目录地址
          cp	复制文件或目录
          mv	移动文件或目录
          less	在文件中翻页
          cat	打印整个文件
          xargs	执行参数值
          find	查找文件
          grep	在文件中查找内容
          man	打开帮助手册
          apropos	查找合适的帮助内容
          env	查看环境
          echo	打印参数值
          export	输出/设置新环境变量
          exit	退出 shell
          sudo	危险！ 获得 root 权限 慎用！
          
          via[附录 A：命令行速成教程 - 附录练习 1 环境配置 - 《笨办法学Python3（Learn Python3 The Hard Way 中文版）》 - 书栈网 · BookStack](https://www.bookstack.cn/read/LearnPython3TheHardWay/spilt.2.spilt.60.learn-py3.md)
          [[20201221]] 上午7:09
    - 应用示例
        - 你已经学习了 pwd 的作用，即“打印工作目录”。^^什么是目录？目录就是文件夹^^，它们是同一个东西。当你打开你电脑的文件查看器去寻找文件的时候，你就是在文件夹中穿梭，这些文件夹就是我说的“目录”。
          via[附录 A：命令行速成教程 - 附录练习 2 路径，文件夹，目录 (pwd) - 《笨办法学Python3（Learn Python3 The Hard Way 中文版）》 - 书栈网 · BookStack](https://www.bookstack.cn/read/LearnPython3TheHardWay/spilt.3.spilt.60.learn-py3.md)
          [[20201221]] 上午7:10
        - 不管你什么时候迷的路，很大可能是因为你输入命令的时候不知道你停在哪儿。你要做的就是输入 pwd 以查看你当前所在的目录，这将会告诉你你现在在哪儿。
          via[附录 A：命令行速成教程 - 附录练习 3 如果你迷路了 - 《笨办法学Python3（Learn Python3 The Hard Way 中文版）》 - 书栈网 · BookStack](https://www.bookstack.cn/read/LearnPython3TheHardWay/spilt.4.spilt.60.learn-py3.md)
          [[20201221]] 上午7:13
        - 现在用 pwd 弄明白你在哪儿，然后用 cd ~ 回到 home，这样可以确保你总是在正确的地方。
          via[附录 A：命令行速成教程 - 附录练习 3 如果你迷路了 - 《笨办法学Python3（Learn Python3 The Hard Way 中文版）》 - 书栈网 · BookStack](https://www.bookstack.cn/read/LearnPython3TheHardWay/spilt.4.spilt.60.learn-py3.md)
          [[20201221]] 上午7:14 cp [-R [-H | -L | -P]] [-fi | -n] [-apvX] source_file target_fileVia[起始页](favorites://) [[20210909]] 下午6:01
        - 
