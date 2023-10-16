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
