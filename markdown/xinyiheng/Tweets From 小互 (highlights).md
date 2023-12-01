- Full Title:: Tweets From 小互
- Category:: #tweets
- URL:: [🔗](https://twitter.com/xiaohuggg)
- ### Highlights first synced by #Readwise [[October 11th, 2023]]
    - 抓紧更新ChatGPT客户端

可以直接获得Voice和DALL·E 3功能

😁 https://t.co/YeynTuLGgP

![](https://pbs.twimg.com/media/F8H5HW9aQAATJgs.jpg) ([View Tweet](https://twitter.com/xiaohuggg/status/1711934048447406282))
- ### New highlights added [[October 16th, 2023]] at 11:01 AM
    - VideoReTalking：让视频中的人物的嘴型与输入的声音同步。

你只需要输入任意一个视频和一个音频文件，它能给你生成一个新的视频，在这个视频里，人物的嘴型会与音频同步。VideoReTalking不仅可以让嘴型与声音同步，还可以根据声音改变视频中人物的表情。整个过程不需要用户干预，都是自动完成的。

工作流程：

整个系统的工作流程分为三个主要步骤：面部视频生成、音频驱动的嘴型同步和面部增强。所有这些步骤都是基于学习的方法，并且可以在一个顺序的流程中完成，无需用户干预。

1、面部视频生成：首先，系统会使用表情编辑网络来修改每一帧的表情，使其与一个标准表情模板相符，从而生成一个具有标准表情的视频。

2、音频驱动的嘴型同步：然后，这个视频和给定的音频一起被输入到嘴型同步网络中，生成一个嘴型与音频同步的视频。

3、面部增强：最后，系统通过身份感知的面部增强网络和后处理来提高合成面部的照片真实性。

项目及演示：https://t.co/1ihBGMtTTA
论文：https://t.co/86fuCMIu4l
GitHub：https://t.co/M4mD77ebUe
Colab在线体验：https://t.co/KytXKx8wtp

该系统是使用 PyTorch 实现的，并且每个模块都是单独训练的。系统在 VoxCeleb 数据集上进行了训练。

VoxCeleb 是一个大型的、多样性丰富的说话头部视频数据集。这个数据集包含了 22,496 个不同身份和头部姿态的说话头部视频。选择这个数据集的目的是为了确保模型能够处理各种各样的说话头部视频。

通过这样详细和精细的训练过程，VideoReTalking 成功地实现了一个能够生成高质量、嘴型与音频同步的说话头部视频编辑系统。 ([View Tweet](https://twitter.com/xiaohuggg/status/1713737733301326044))
- ### New highlights added [[October 17th, 2023]] at 11:13 AM
    - Deep Chat：能够轻松地将AI聊天机器人嵌入到任何网站中。

Deep Chat一个完全可定制的 AI 聊天组件，可以连接到任何API，使用它直接从浏览器与流行的AI机器人进行通信，或者你自己的定制服务。

除了基础的文本聊天外，还支持文件传输、音频录制、摄像头照片捕捉等多媒体交互。

界面高度可定制，支持多种 UI 框架/库，从界面到功能几乎所有元素都可按需进行定制。

它是一个全面、多功能的聊天解决方案，适用于各种需要增加交互性和功能的网站。无论您的网站是使用哪种编程语言或框架（如 React、Vue、Angular 等）构建的，都可以方便地集成 Deep Chat。

主要特点：

1、多媒体交互: Deep Chat 支持发送和接收文件，这对于需要文件共享功能的应用场景非常有用。例如，客户可以直接通过聊天窗口发送文档或图片。

2、音频和视频捕捉：该组件允许通过网络摄像头和麦克风进行照片和音频捕捉。这可以用于实现更丰富的用户交互，如视频聊天或语音指令。

3、语音到文本和文本到语音：它支持语音到文本（Speech To Text）和文本到语音（Text To Speech）功能，这意味着用户可以用语音输入消息，并听到机器人的语音回应。

4、高度可定制的 UI:：Deep Chat 允许您自定义聊天界面的外观和感觉，以匹配您网站的品牌和设计。

5、跨平台和跨框架：由于它是与框架无关的，因此可以轻松地集成到几乎任何现代网页框架中，如 React、Vue、Angular 等。

6、开放源代码和社区支持： 作为一个开源项目，您可以根据需要修改源代码，或者参与到社区中，以贡献新的功能或改进。

7、即时消息和通知：可以设置即时消息和通知，以便在有新消息或事件发生时立即通知用户。

8、安全性和隐私: 虽然这主要取决于您如何配置和部署它，但 Deep Chat 设计上考虑了安全性和隐私，允许加密通信和安全的数据存储。

GitHub：https://t.co/8OGeqjOSSM
网站：https://t.co/rl4wn2G36d ([View Tweet](https://twitter.com/xiaohuggg/status/1713922172559970541))
- ### New highlights added [[October 17th, 2023]] at 2:10 PM
    - Pi

现在

可以联网了…👏

可以访问网络上最新的信息了… https://t.co/OrYAEQ0Gan ([View Tweet](https://twitter.com/xiaohuggg/status/1714139977976885398))
- ### New highlights added [[October 24th, 2023]] at 8:53 AM
    - 一个可以突破版权限制，让DALL·E 3画出日本动画片水准的方法！

Prompt结构如下：

指定目标受众 ： (少年)
目标受众：年轻男孩（通常年龄 12-18 岁）

指定你需要输出内容的特征：
特征：故事情节动感十足，以友谊和毅力为主题

给出实例动画片：
系列示例：《火影忍者》、《龙珠》、《海贼王》

然后最后可以再加上具体Prompt情节描述：

例如：一只狗和一个男人去冒险...

以下是英文版本Prompt具体风格实例，套用即可，也可以让GPT帮你写，最好用英文，因为效果更好：

👉Japanese Anime Styles (according to ChatGPT): 

Shonen (少年) 
Target Audience: Young boys (typically ages 12-18)
Characteristics: Action-packed stories, themes of friendship and perseverance
Example Series: "Naruto", "Dragon Ball", "One Piece"

Shojo (少女)
Target Audience: Young girls (typically ages 12-18)
Characteristics: Romantic plots, emotional depth, often has intricate art
Example Series: "Sailor Moon", "Fruits Basket", "Ouran High School Host Club"

Seinen (青年)
Target Audience: Adult men (18+)
Characteristics: More mature themes, can include gore, psychological elements, and deep philosophical questions 
Example Series: "Berserk", "Tokyo Ghoul", "Black Lagoon"

Josei (女性) 
Target Audience: Adult women (18+)
Characteristics: Realistic romance, deals with women's issues, often more mature and dramatic
Example Series: "Nana", "Paradise Kiss", "Honey and Clover"

Mecha (メカ) 
Characteristics: Focuses on robots or mechanical suits Themes: War, technology, and the relationship between humans and machines
Example Series: "Mobile Suit Gundam", "Neon Genesis Evangelion", "Code Geass"

Isekai (異世界)
Characteristics: Protagonist gets transported to, reborn, or trapped in a parallel universe or fantasy world 
Themes: Adventure, magic, battles, and adapting to a new world
Example Series: "Re:Zero", "Sword Art Online", "No Game No Life"

Slice of Life (スライス・オブ・ライフ)
Characteristics: Depicts everyday life scenarios, often with a touch of humor or drama
Themes: Friendship, love, challenges of daily life
Example Series: "Clannad", "March Comes in Like a Lion", "Barakamon"

Chibi (ちび or チビ)
Characteristics: Characters are drawn in a cute, small, and deformed manner, often with big heads and tiny bodies Used for comedic effect or to depict childlike cuteness 
Example Series: "Attack on Titan: Junior High", "Hetalia", "Dragon Ball SD"

以上信息来自 @LearnAI_MJ ([View Tweet](https://twitter.com/xiaohuggg/status/1716353451989536897))
- ### New highlights added [[December 1st, 2023]] at 2:52 PM
    - WeChatMsg：一个提取微信聊天记录的工具

它可以将微信聊天记录导出为HTML、Word、CSV格式的文档，并对聊天记录进行分析，生成年度聊天报告等！

感觉可以用来导入到GPTs，克隆一个自己😂

主要功能：

1.破解微信数据库：该工具能够破解手机（安卓或苹果）和PC端微信的数据库。

2.还原微信聊天界面：支持将文本、图片和表情包等内容还原为微信聊天界面的样式。

3.导出聊天记录：用户可以将聊天记录导出为HTML、Word、CSV等格式的文档，方便永久保存。

4.聊天数据分析：工具提供了对聊天数据的分析功能，可以生成可视化的年度聊天报告。

5.项目正在持续更新中，未来可能会支持更多功能，如导出全部表情包、合并多个备份数据等。

GitHub：https://t.co/oN4BFAbgoc<img src='https://pbs.twimg.com/media/GAMUbzqbIAA6v5N.jpg'/> ([View Tweet](https://twitter.com/xiaohuggg/status/1730249158605594870))
