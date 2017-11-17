### vim插件之NerdTree

><b>Description:介绍</b><br>
    NerdTree是一个打开目录的插件,可以快速打开目录下的文件,截图如下:

![NerdTree插件](http://images.vimkid.com/1_100/7_1.jpg "NerdTree插件")

><b>Download:下载地址</b><br>
    https://github.com/scrooloose/nerdtree
[![下载地址](https://github.com/scrooloose/nerdtree "NerdTree")](https://github.com/scrooloose/nerdtree)

><b>Install:安装方法</b><br>
    下载github上对应的文件
    将下载好的文件下的autoload,doc,plugin,等目录下的文件,copy到vim安装目录下的每个对应的目录下即可

#### 打开NerdTree快捷键
    :NERDTreeToggle回车  # 打开或关闭NerdTree
    
#### NerdTree面板中常用快捷键操作
    Enter       # 打开焦点下的文件或目录
    o           # 打开焦点下的文件或目录
    x           # 收起目录
    ?           # 打开帮助文件
    q           # 退出NerdTree
    /           # 在NerdTree列表中快速查找
    hjkl        # 上下左右移动焦点
    ctrl+d      # 向下翻半屏
    ctrl+u      # 向上翻半屏
    u           # 向上一个目录
    C           # 进入焦点目录
    r           # 刷新当前焦点下的文件
    R           # 刷新当前根目录下的所有文件
    m           # 显示操作菜单
    ma          # 新建一个文件
    mm          # 重命名一个文件
    B           # 打开书签

#### NerdTree面板中不常用操作
    go          # 预览
    t           # 在新标签中打开,进入文件
    T           # 在新标签中打开,不进入文件
    i           # 以横向分割方式打开
    gi          # 以横向分割方式打开预览
    s           # 以纵向分割方式打开
    gs          # 以纵向分割方式打开预览
    X           # 收起所有子目录
    e           # 浏览目录的文件
    P           # 焦点跳到根目录
    p           # 焦点跳到父目录
    J           # 焦点跳到当前目录最后一个文件
    K           # 焦点跳到当前目录第一个文件
    I           # 隐藏文件
    f           # 文件过滤

><b>Tipds:NerdTree帮助</b><br>
    NerdTree帮助文件比较齐全，在neerdtree面板下按下? 即可打开帮助,截图如下:

![NerdTree插件](http://images.vimkid.com/1_100/7_2.jpg "NerdTree插件")

#### BookMark(书签操作)
    :Bookmark <name>      # 将当前文件添加到书签，并命名为name ,name 可改成其他
    :ClearBookmarks       # 清除书签
    :ClearAllBookmarks    # 清除所有书签

#### NerdTree vimrc配置 
    let NERDChristmasTree = 1    # 让nerdtree彩色显示

#### 推荐映射 (写到vimrc 下)
    nmap ;j :NERDTreeToggle<cr>    # 按;j 打开或关闭NerdTree
    
