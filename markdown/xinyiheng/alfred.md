- Alfred 的脚本通过[[ Workflows ]]功能中的 Run Script Action 执行，支持 [[Bash]]、PHP、Ruby、[[python]]、Perl、[[AppleScript]] 和[[JavaScript]]等多种语言。Via[极具潜力的效率启动器 App，Raycast 脚本功能详解 - 少数派](https://sspai.com/post/64339)[[20210105]] 下午5:17
- 非常建议大家在 iCloud Drive 或者你其它常用的云同步应用中新建一个文件夹用于存放脚本。这会极大地方便你在不同设备之间^^同步创建的自定义脚本^^。Via[极具潜力的效率启动器 App，Raycast 脚本功能详解 - 少数派](https://sspai.com/post/64339)[[20210105]] 下午5:20
- 制作一个简单的workflow
    - 目的：复制网页名称和地址，以markdown的格式呈现
    - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FZKdg8CktRT.png?alt=media&token=3cf8bad7-e2de-4adf-abe4-bb59942145f6)
    - Triggers: Snippet
[[Snippet ]]是「^^快捷短语^^」，如果将它作为触发器，在打字输入指定短语后会立刻执行后续动作。在这里我将短语设置为 url，用来触发后续的动作 Run Script。
在 Snippet 这个触发器中，默认前缀设置为 \\，那么当你需要触发短语时，就需要在你设置的短语前加上这个前缀，比如在这个 Workflow 中我需要输入 \\url 才会成功触发下一个动作。
至于为什么用 Snippet Trigger 嘛，因为可以省去使用快捷键唤出 Alfred 这一步，这样一来就不会打断写作过程了。Via[从 0 到 1 写一个 Alfred Workflow - 少数派](https://sspai.com/post/47710)[[20210105]] 下午5:27
- #[[参考资料]]
    - Alfred WorkflowsVia[Alfred Workflows - Alfred App Community Forum](https://www.alfredforum.com/forum/1-alfred-workflows/)[[20210105]] 下午5:33
- 类似软件
    - [[raycast]]
    - [[launchbar]]T0210108]] 上午11:48
    - 0 到 1 写一个 Alfred WorkflowVia[从 0 到 1 写一个 Alfred Workflow - 少数派](https://sspai.com/post/47710)[[20210108]] 上午11:48
    - 
