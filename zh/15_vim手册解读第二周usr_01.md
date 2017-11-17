><b>Tips:</b><br>
    本文只是摘取vim英文文档作者认为比较有用的精华进行解读, 并不是全文详细翻译,如想看全文详细翻译,请参照vim中文文档,解读的文档版本为vim8.0. 文档位置为"vim安装目录/doc/usr_**.txt"

## 第二周   
><b>介绍:</b><br>
    本文对vim手册 usr_01.txt (1 ~ 192 行文档解读)
    本文介绍了vim 手册相关的一些内容

### 01.1 两种手册 ( Two manuals )

><b>两种手册:</b><br>
    这里面介绍了两种,手册, 一种是用户手册,一种是参考手册,用户手册主要面向解释,从易到难,像读书本一样.参考手册则是精确描述vim 的工作机理.

    CTRL-]    # 跳入光标下的主题内容
    CTRL-O    # 跳回

### 01.2 关于Vim安装 (Vim installed)

><b>vimrc路径:</b><br>
    这个小节介绍了vimrc 的路径,分别介绍了Unix, MS-DOS,Amiga 三种操作系统下vimrc 配置文件的设置方法,详情可以自行参考文档usr_01.txt. vimrc 配置文件一般放在`$VIM`目录下,如/usr/local/share/vim/vimrc,可以通过以下命令查找具体目录路径.

    :echo $VIMRUNTIME      # vim 运行路径如:/usr/local/share/vim/vim80
    :echo $VIM             # vim 主目录路径如:/usr/local/share/vim
    :set compatible?  #  如果显示 nocompatible  表示正确
    :scriptnames      # 显示加载的vim 插件和脚本

### 01.3 Vim 快速入门 (Using the Vim tutor)

><b>vim 30分钟入门教程:</b><br>
    本小节介绍了vim快速入门文档,相当实用, 支持多种语言,如中文,英语,法语等.  在命令行输入以下命令即可进入文档.命令后加国家语言参数即可查看不同语言的文档. 

    vimtutor         # vim 30 分钟入门教程 英文版
    vimtutor zh      # vim 30 分钟入门教程 中文版
    vimtutor fr      # vim 30 分钟入门教程 法文版
    gvimtutor        # GUI用户可以用该命令 
    vimtutor -g      # GUI用户可以用该命令 

><b>Vim 30分钟入门教程在线文档链接:</b><br>


