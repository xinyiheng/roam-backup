- #[[基本功能]]
    - 手机投屏到电脑，并且在电脑上控制手机
- #[[使用方法]]
    - 安装方法参考这个视频：____ — via [scrcpy安装方法](https://mp.weixin.qq.com/s?__biz=MzU1NDgyNDQ1Ng==&mid=2247495397&idx=3&sn=4eedfeaad8afb0749ebe86f5b86c7609&chksm=fbdf0882cca8819408cb6774619bc9a2364474b5ce8423cf1111089c7614dc2ded0449353eea) +Roam
- #[[个人评价]]
    - 我所了解的最棒的投屏软件，画质高清，毫无卡顿，还完全免费。可以在windows和mac上使用。
- 在电脑上操作手机
    - 可以使用vysor，付费版一年10美元，目前还没有付费，因为没有确定是否是刚需。
    - 目前找到的最佳方式是使用scrcpy，我目前很满意。具体实现方法保存在印象笔记当中了。[安装scrcpy的方法。](https://app.yinxiang.com/shard/s63/nl/13797828/2b04f36c-352a-475a-8366-e0abada15e96/)
    - 其中难点是安装[[Homebrew]]，我当初差点因为安装这个软件而放弃。[安装方法见链接。](https://app.yinxiang.com/shard/s63/nl/13797828/a6e548b3-5f83-4a2a-8598-90de6637b640/)
        - 2022年10月17日 好久没用，发现上面的失效了。按照这个重新安装成功https://www.jianshu.com/p/e0471aa6672d
    - 很长时间没用之后发现无法连接，提示错误。我按照指示操作发现了原因。原来是手机没有开启开发者模式中的usb调试。开启之后就好了，可能买了小米手机之后我就没用过这个功能。
        - wangxiaohuideMacBook-Pro:~ wangxiaohui$ scrcpy
          2021-08-15 20:13:23.764 scrcpy[27360:553358] INFO: scrcpy 1.16 <https://github.com/Genymobile/scrcpy>
          adb: error: failed to get feature set: no devices/emulators found
          2021-08-15 20:13:23.771 scrcpy[27360:553358] ERROR: "adb push" returned with value 1
    - Frequently Asked QuestionsVia[scrcpy/FAQ.md at master · Genymobile/scrcpy · GitHub](https://github.com/Genymobile/scrcpy/blob/master/FAQ.md#adb-issues) [[20210815]] 下午8:26
    - 快捷键Via[Scrcpy-Android 设备投屏+控制工具 - 农夫山药 - 博客园](https://www.cnblogs.com/fanfeng/p/13093465.html) [[20210815]] 下午8:29
        - 最常用到的是熄灭手机屏幕cmd+o@评论:资料里的写的都是ctrl，用mac其实应该是cmd
        - 打开手机屏幕cmd+shift+o
        - 注意，这些快捷键在外接的蓝牙键盘上使用没有反应，必须在macbook自带的键盘上使用才有反应。很神奇。
