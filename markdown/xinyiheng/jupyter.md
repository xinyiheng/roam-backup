- 本篇将给大家介绍一款超级好用的工具：Jupyter notebook。
  
  为什么要介绍这款工具呢？
  
  如果你想使用Python学习数据分析或数据挖掘，那么它应该是你第一个应该知道并会使用的工具，它很容易上手，用起来非常方便，是个对新手非常友好的工具。而事实也证明它的确很好用，在[[数据挖掘平台]][[ Kaggle ]]上，使用 Python 的数据爱好者绝大多数使用 jupyter notebook 来实现分析和建模的过程，因此，如果你想学习机器学习，数据挖掘，那么这款软件你真的应该了解一下。
  via[Jupyter notebook快速入门教程 - 知乎](https://zhuanlan.zhihu.com/p/36764170)
  [[20201214]] 下午4:49
- Jupyter notebook 是一种 Web 应用，它能让用户将说明文本、数学方程、代码和可视化内容全部组合到一个易于共享的文档中，非常方便研究和教学。在原始的 Python shell 与 IPython 中，可视化在单独的窗口中进行，而文字资料以及各种函数和类脚本包含在独立的文档中。但是，notebook 能将这一切集中到一处，让用户一目了然。
  via[Jupyter notebook快速入门教程 - 知乎](https://zhuanlan.zhihu.com/p/36764170)
  [[20201214]] 下午4:54
- Jupyter Notebook 本质上是一个开源的 [[Web 应用]]，支持但不限于实时代码展示、可视化、Markdown 等功能，这就意味着你可以用 JavaScript 对其进行改造（比如有人移植了echarts），也可以很好的将其移植。因此基于这些特性，可以将 Jupyter Notebook 很轻易地部署在网页或服务器上运行。
  via[在线的 Jupyter Notebook 云环境 - 少数派](https://sspai.com/post/55402)
  [[20201214]] 下午5:28
- 在[[数据科学]]领域，[[R 语言]]和  往往都是新手入门的选择。像我这样的「两栖动物」，可能有时两者都用到，因此我希望的云环境可以将二者都集成。恰好Jupyter Notebook 都支持运行这二者的内核。
  via[在线的 Jupyter Notebook 云环境 - 少数派](https://sspai.com/post/55402)
  [[20201214]] 下午5:28
- 当然，如果你只想在自己的电脑上进行操作学习，又想避免环境搭建的许多麻烦，那么其实安装 [[Anaconda]] 后就可以直接「开箱即用」。但是原始的 Jupyter Notebook 如果没有其他插件辅助的话，可能仅仅就是一个单一的编辑器，所以仍然还需要额外的插件才能让使用上更接近于 [[IDE]]（集成开发环境）
  via[在线的 Jupyter Notebook 云环境 - 少数派](https://sspai.com/post/55402)
  [[20201214]] 下午5:31
- 原始的 Jupyter Notebook 如果没有其他插件辅助的话，可能仅仅就是一个单一的编辑器，所以仍然还需要额外的插件才能让使用上更接近于 IDE（集成开发环境）
  
  好在已经有人用 JavaScript 替我们写好了插件，你可以在 Github 上搜索到jupyter_contrib_nbextensions插件，然后按照官方文档只输入两行命令后即可搞定
  pip install jupyter_contrib_nbextensions # 也可以使用 conda 安装，详见官方文档
  jupyter contrib nbextension install --user
  安装好后只需要重新进入 Jupyter Notebook 的主页，就可以看到「NBextensions」选项，点击进入到选项之中即可以勾选喜欢的插件来提高你的编程体验了！
  via[在线的 Jupyter Notebook 云环境 - 少数派](https://sspai.com/post/55402)
  [[20201214]] 下午5:41
- 学习数据分析的第一关是什么？
    - 每当我打开在收藏夹里吃灰的数据分析或[[数据科学]]的资源时，就会发现每一个教程总是绕不开 「[[环境搭建]]」的部分。不可否认的是，好的编程环境可以让学习者更好地体验编程学习的乐趣；但环境搭建又往往不可避免的存在很多坑，也许没等一个环境搭建好，就在当中遇到各种奇奇怪怪的问题，学习的兴致早就被报错折磨殆尽了。所以，不得不说环境搭建对于新手而言往往兴趣的 Killer。
      via[在线的 Jupyter Notebook 云环境 - 少数派](https://sspai.com/post/55402)
      [[20201214]] 下午5:37
- 
