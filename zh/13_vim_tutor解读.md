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
    :s/old/new/g  # 替换old为new

    
    

    





><b>Vim tutor 原文中文文档链接:</b><br>
[![Vim快速入门中文文档](http://www.vimkid.com/zh/14.html "Vim Tutor")](http://www.vimkid.com/zh/14.html)       http://www.vimkid.com/zh/14.html  <br/>
[![Vim快速入门英文文档](http://www.vimkid.com/14.html "Vim Tutor")](http://www.vimkid.com/14.html)       http://www.vimkid.com/14.html


