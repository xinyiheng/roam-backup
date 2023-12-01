- Full Title:: Tweets From 宝玉
- Category:: #tweets
- URL:: [🔗](https://twitter.com/dotey)
- ![](https://pbs.twimg.com/profile_images/561086911561736192/6_g58vEs.jpeg)
- ### Highlights first synced by #Readwise [[December 1st, 2023]]
    - #AI开源项目推荐：VikParuchuri/marker

Marker 能将 PDF、EPUB 和 MOBI 文件转换成 markdown 格式。它的转换速度是 nougat 的十倍之快，对多数文档的处理更为精确，且几乎不会产生错误的幻觉效果。

- 支持多种类型的 PDF 文档（特别优化了对书籍和科学论文的处理）
- 可以去除页眉、页脚和其他无关内容
- 能够将大部分公式转换成 latex 格式
- 格式化代码块和表格
- 支持多种语言（主要测试语言为英语）
- 可在 GPU、CPU 或 MPS 上运行

工作原理

Marker 是基于一系列深度学习模型构建的：

- 提取文本，必要时使用 OCR 技术（采用启发式算法和 tesseract 工具）
- 检测页面布局（使用 [布局分割器](https://t.co/CqHMbaR6lQ) 和 [列检测器](https://t.co/NI5M14bERX)）
- 清洗并格式化每一块内容（运用启发式算法和 [nougat](https://t.co/vMhQL8OaOX)）
- 合并这些块并对整体文本进行后期处理（利用启发式算法和 [pdf后处理器](https://t.co/K6Wq5m9afk)）

依赖自回归前向传递来生成文本的方法通常速度较慢，且容易出现重复或虚假内容。根据 nougat 论文的研究，这种重复现象在测试集的页面中出现的比例为 1.5%，但在非专业领域的文档中，这一比例会更高。根据我的个人测试，非专业领域（非 arXiv）的页面重复率超过了 5%。

尽管 nougat 模型表现出色，但我还是希望找到一个更快、更适用于普通用途的解决方案。Marker 的转换速度是 nougat 的十倍，因为它只对公式块进行 LLM 前向传递处理，所以几乎没有产生错误幻觉的风险。

项目地址：https://t.co/UI3w2R9eQ4 ([View Tweet](https://twitter.com/dotey/status/1730418206991409407))
