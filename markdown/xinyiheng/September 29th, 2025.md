- #[[技能]]
    - 我很喜欢豆包桌面端 ai 播客那种不遗漏文章中的任何部分，只不过是把原文改成双人对谈的播客的形式。但是我发现这种音频实际上是点击之后开始生成的，无法直接下载。我知道用 blackhole 2ch 来录制。一起没有掌握好，觉得设置很麻烦。现在看还好。
        - ## 一、创建「多输出设备」
            - 目的：让声音同时走 **耳机/音箱**（你能听到），又走 **BlackHole**（录音软件能收到）。
                1. 在 **Audio MIDI 设置** 左下角，点击 **+** → 选择 **创建多输出设备**。
                2. 在右侧勾选：
                    - **BlackHole 2ch**
                    - 你的真实输出设备（比如 `Mac mini 扬声器` 或蓝牙耳机 `F162`）
                3. 把「多输出设备」重命名一下（比如叫 `播客录制输出`，方便识别）
                4. ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2F5rk71_fJvc.png?alt=media&token=e29d791b-0628-410c-bd5a-1c14def8531e)
        - ## 二、切换系统声音输出
            1. 打开 **系统设置 → 声音 → 输出**，把输出设备改成刚才创建的「多输出设备」。
            2. 现在系统所有声音（包括豆包 AI 播客）会同时送到耳机/音箱和 BlackHole。
            3. ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FZJMh07CpyK.png?alt=media&token=d265fbb0-0e47-40f0-9e5d-6d91fff2a364)
        - ## 三、用quicktime来录制音频，新建录音
            - 我设置了一个 keyboard maestro 快捷方式，用 ly 来快速创建
    - 获得桌面端 ai 播客效果的可能另一个途径有时有效的做法是，先把财新文章用飞书剪藏，去除一些财新内嵌进去的提示词，然后打印成 pdf，在豆包 ai 播客界面上传 pdf 也可以，但不一定是完整版的。
    - 为了获得更好的效果，我开始整理提示词，我用 keyboard maestro 新建了一个名为提示词的宏组，快捷键都设置为 tsc，这样，就可以一下子展示所有提示词，然后挑选备用。但这个方式中，豆包对于内容审核有时严格，会拒绝生成 ai 播客。
    - 
