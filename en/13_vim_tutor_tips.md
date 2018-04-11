><b>Tips:</b><br>
    本文只是摘取vim英文文档作者认为比较有用的精华进行解读, 并不是全文详细翻译,如想看全文详细翻译,请参照vim中文文档,解读的文档版本为vim8.0. 文档位置为"vim安装目录tutor/tutor.txt"

## Vim Tutor 整理解读
><b>介绍:</b><br>
    本文对vim手册 tutor/tutor.txt (1 ~ 996 行文档解读)
    本文介绍了vim 的一个快速入教程20-30分钟入门
    本文对是该教程的一个压缩整理
    阅读本文前请先对vim的模式进行了解，主要了解插入模式(insert)和普通模式　（normal)

### 01 第一讲 
    j       # 光标向下移动
    k       # 光标向上移动
    l       # 光标向右移动
    h       # 光标向左移动
    <ESC>   # 进入normal 普通模式
    :q!     # 退出编辑
    x       # 删除光标所在位置的一个字符
    i       # 从普通模式进入插入模式,插入模式可以输入内容
    A       # 从行尾进行添加,并进入插入模式
    :wq     # 保存退出


### 02 第二讲 
    dw      # 删除一个单词
    d$      # 从当前光标删除到行末
    w       # 向前移动一个单词
    2w      # 向前移动两个单词
    3w      # 向前移动三个单词
    0       # 移动光标到行首
    d2w     # 删除两个单词
    dd      # 删除一行
    2dd     # 删除两行
    u       # 撤销改动,按一次撤销一次
    U       # 撤销一行所有的改动
    Ctrl-U  # 重做撤销

><b>第二讲涉及语法:</b><br>
    d [number] motion

### 03 第三讲 
    p       # 将最后一次删除或复制的内容粘贴
    r       # 替换一个字符
    ce      # 删除一个单词并进入插入模式
    cw      # 删除一个单词并进入插入模式

><b>第三讲涉及语法:</b><br>
    c [number] motion

### 04 第四讲 
    Ctrl-g  # 显示当前编辑文件中当前光标所在行位置以及文件状态信息。
    /       # 正向搜索命令,如/hello  查找文中的hello, 按n 查找下一个
    ?       # 反向搜索,同上
    Ctrl-o  # 回到上一个编辑的位置,重复按回退多步
    Cgrl-i  # 跳传到较新的位置
    %       # 可以查找配对的括号 )、]、} 
    :s/old/new/g  # 替换old为new, 不需要确认
    :s/old/new/gc  # 替换old为new 并逐个确认

### 05 第五讲 
    :!       # 执行外部命令
    :!ls     # 执行一个ls命令
    :w TEST  # 保存文件，将文件命名为TEST
    :!del TEST  # MS-DOS下删除TEST文件
    :!rm  TEST  # Unix  下删除TEST文件
    :r TEST    # 提取TEST文件内容
    :r !ls     # 提取ls 命令的输出

    
### 06 第六讲 
    o    # 在光标的下方打开新的一行并进入插入模式 
    O    # 在光标的上方打开新的一行并进入插入模式 
    a    # 在光标之后插入文本
    A    # 可以在光标所在行的行末之后插入文本。
    R    # 可连续替换多个字符按Esc退出替换
    y    # 复制文本
    e    # 使光标移动到单词末尾
    p    # 粘贴文本
    /    # 进入查找, 按n 进入查找下一个
    :set ic     # 查找忽略大小写 
    :nohlsearch  # 移除匹配欺罔的高亮显示
    
><b>第三讲涉及选项:</b><br>
    :set xxx    ＃ 设置选项


### 07 第七讲 
    ctrl+w    # 在窗口之间跳转    
    F1        # 打开帮助文件
    HELP      # 打开帮助文件
    :help     # 打开帮助文件
    :help w   # 打开关于w 的帮助
    :help c-CTRL-D   ＃ 打开ctrl-D 快捷键的帮助
	:help insert-index
	:help user-manual
    :q         # 关闭帮助窗口
	:help cmd   # 打开cmd命令的帮助 
    :help vimrc-intro   # vimrc文件帮助
    :edit ~/.vimrc		# 这是 Unix 系统打开vimrc配置文件所使用的命令
    :edit $VIM/_vimrc	# 这是 MS-Windows 系统打开vimrc配置文件所使用的命令
    :write    # 保存文件同  :w 一样 
    ctrl-d    # 命令模式下提示相关命令列表
    TAB       # 补全命令









