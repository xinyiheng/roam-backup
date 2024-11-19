- Author:: [[勇哥碎碎念]]
- Full Title:: Macos下的容器、宗卷、分区的主要区别及硬盘分区建议 - 知乎
- Category:: #articles
- URL:: https://zhuanlan.zhihu.com/p/596119469
- ### Highlights first synced by #Readwise [[March 4th, 2023]]
    - macos下的容器、宗卷、分区的主要区别及硬盘分区建议
    - 如上图所示，所有宗卷共享同一个容器的存储空间，如果用户不进行增加分区的操作，那么此容器会占用此硬盘的几乎所有空间。
      
      如果用户继续对硬盘进行增加分区操作，当指定分区格式为apfs格式时，系统会新增一个容器，并在容器内增加一个APFS宗卷，当指定分区格式为非apfs格式时，系统会新增一个相应格式的分区。
      
      容器就相当于分区，只是两者所对应的文件系统不一样。
