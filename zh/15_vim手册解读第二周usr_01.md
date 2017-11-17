><b>Tips:</b><br>
    本文只是摘取vim英文文档作者认为比较有用的精华进行解读, 并不是全文详细翻译,如想看全文详细翻译,请参照vim中文文档,解读的文档版本为vim8.0. 文档位置为"vim安装目录/doc/usr_**.txt"

## 第二周   
><b>介绍:</b><br>
    usr_01.txt (1 ~ 192 行文档解读)
    本文介绍了vim 手册相关的一些内容

### 01.1 两种手册 ( Two manuals )

><b>两种手册:</b><br>
    这里面介绍了两种,手册, 一种是用户手册,一种是参考手册,用户手册主要面向解释,从易到难,像读书本一样.参考手册,精确描述vim 的工作机理

    CTRL-]    # 跳入光标下的主题内容
    CTRL-O    # 跳回
    

### 01.2 关于Vim安装 (Vim installed)

><b></b><br>
    这个小节介绍了vimrc 的路径,分别介绍了Unix, MS-DOS,Amiga 三种操作系统下vimrc 配置文件的设置方法,详情可以自行参考文档usr_01.txt. vimrc 配置文件一般放在`$VIM`目录下,如/usr/local/share/vim/vimrc,可以通过以下命令查找具体目录路径.

    :echo $VIMRUNTIME      # vim 运行路径如:/usr/local/share/vim/vim80
    :echo $VIM             # vim 主目录路径如:/usr/local/share/vim
    :set compatible?  #  如果显示 nocompatible  表示正确
    :scriptnames     # 显示加载的vim 插件和脚本

### 01.3 Using the Vim tutor
    vimtutor        # vim 30 分钟入门教程


