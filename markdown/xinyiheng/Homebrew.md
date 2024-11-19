- 如何安装Homebrew？
    - 其中难点是安装[[Homebrew]]，我当初差点因为安装这个软件而放弃。[安装方法见链接。](https://app.yinxiang.com/shard/s63/nl/13797828/a6e548b3-5f83-4a2a-8598-90de6637b640/)
        - 2022年10月17日 好久没用，发现上面的失效了。按照这个重新安装成功https://www.jianshu.com/p/e0471aa6672d
- Homebrew可以用来做什么？
    - 直接在终端中通过命令来安装软件，省去了下载软件，解压和拖拽进入"应用程序"文件夹的麻烦。
- Homebrew 在 2009 年由马克斯·霍威尔（Max Howell）写成，它在 GitHub 上拥有大量贡献者，目前仍处于活跃状态。
  via[再谈 Homebrew Cask 在 macOS 上安装应用的轻松感 - 少数派](https://sspai.com/post/40321)
  [[20201216]] 下午11:05
- 可惜的是，我们读到的文章往往止步于 brew install 某某应用[^1]（用 HomeBrew 安装应用）这一条命令。
  via[9 条进阶命令，把 HomeBrew 打造成管理第三方应用的 App Store - 少数派](https://sspai.com/post/43451)
  [[20201216]] 下午10:59
- 可以实现那些功能？
    - 更新应用和清理旧版
      via[9 条进阶命令，把 HomeBrew 打造成管理第三方应用的 App Store - 少数派](https://sspai.com/post/43451)
      [[20201216]] 下午11:01
        - 更新完后可以运行一下下面的命令，把应用的旧版本和缓存删除。
          
          brew cleanup
          via[9 条进阶命令，把 HomeBrew 打造成管理第三方应用的 App Store - 少数派](https://sspai.com/post/43451)
          [[20201216]] 下午11:02
        - 如果你只是想看看有哪些应用可以清理，但暂时不需要处理它们，则可以通过这个命令一窥究竟：
          
          brew cleanup -n
          via[9 条进阶命令，把 HomeBrew 打造成管理第三方应用的 App Store - 少数派](https://sspai.com/post/43451)
          [[20201216]] 下午11:03
    - 访问应用官网
      via[9 条进阶命令，把 HomeBrew 打造成管理第三方应用的 App Store - 少数派](https://sspai.com/post/43451)
      [[20201216]] 下午11:02
    - 搜索应用
      via[9 条进阶命令，把 HomeBrew 打造成管理第三方应用的 App Store - 少数派](https://sspai.com/post/43451)
      [[20201216]] 下午11:02
    - [[Homebrew Cask ]]是 Homebrew 的扩展，借助它可以方便地在 macOS 上安装图形界面程序，即我们常用的各类应用。Homebrew 中文含义为自制、自酿酒，Cask 中文含义为桶、木桶，桶装酒是一种成品，也就是说每一个 homebrew cask 都可以直接使用的，比如 Atom 的 Cask 名称为 atom，那么就可以使用如下命令安装：
      
      brew cask install atom
      via[再谈 Homebrew Cask 在 macOS 上安装应用的轻松感 - 少数派](https://sspai.com/post/40321)
      [[20201216]] 下午11:06
