- conda分为anaconda和miniconda。anaconda是包含一些常用包的版本（这里的常用不代表你常用 微笑.jpg），miniconda则是精简版，需要啥装啥，所以推荐使用miniconda。
  
  作者：卖萌哥
  链接：https://www.jianshu.com/p/edaa744ea47d
  来源：简书
  著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
  via[conda的安装与使用（2020-08-10更新） - 简书](https://www.jianshu.com/p/edaa744ea47d)
  [[20201214]] 下午10:49
- Conda 常用命令
  Anaconda 附带的 conda 命令除了用来管理各种 Python 的相关包和库以外，还能用来创建虚拟环境等。之后所有操作都可以通过命令行地方式来实现。这里给出常用的命令以及功能描述，详见表格：
  via[01 环境配置与运行 - 少数派](https://sspai.com/post/61799)
  [[20201214]] 下午6:02
- 安装了anaconda但是无法使用conda命令怎么办？
    - 网上有很多答案，但是有些好用，有些不好用。我利用下面这个成功解决了问题
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2FhKWxHNA9ZR.png?alt=media&token=4abb9362-135a-4e8b-adbc-cae3f3234af7)
        - 我的解决方案是：
          
          1. 终端输入：
          source ~/.bash_profile 
          就能进入（base）环境了，在（base）环境中就可以使用conda了
                  然后使用 source deactivate 或 conda deactivate 退出，再输入conda就能看到conda的信息了，说明conda在外部环境也可以使用了。（这个方法蛮玄学，但是抓到耗子就是好猫）
                  一般出现这个bug，网上的解决方案是：vi ~/.zshrc （如简书上的：https://www.jianshu.com/p/13f5d20e61f8）
          
          我从来没有用过vim（听说很好用），而且这个命令我输入进去，结果并不是像上述简书中说的那样，所以这个方法放弃了。
          
          via[(4条消息) MAC OS 安装anaconda之后 conda命令无效_Cece11011的博客-CSDN博客](https://blog.csdn.net/Cece11011/article/details/103820337)
          [[20201214]] 下午11:23
        - 
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fxinyiheng%2F5QTOf00Nvx.png?alt=media&token=dfe7ce60-3b25-4092-9029-6c6c5430766a)
