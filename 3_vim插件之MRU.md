###vim插件之MRU

><b>Description:介绍</b><br>
    MRU是一个经典的老插件,可以快速打开最近打开过的文件截图如下:

![MRU插件](http://images.vimkid.com/1_100/3_1.jpg "MRU插件")

><b>Download:下载地址</b><br>
    http://www.vim.org/scripts/script.php?script_id=521 
[![下载地址](http://www.vim.org/scripts/script.php?script_id=521 "MRU")](http://www.vim.org/scripts/script.php?script_id=521)

><b>Install:安装方法</b><br>
    将下载好的`mru.vim` 插件放到vim安装目录下的`plugin`目录下即可

####打开MRU快捷键
    :MRU回车           # 打开MRU历史记录列表
    :MRU pattern<tab>  # 用匹配的方式提示打开文件
    
####MRU中快捷键操作
    jk          # 在历史记录列表中上下移动
    Enter       # 进入相应文件
    t           # 在新标签中打开历史文件
    u           # 更新文件列表
    q           # 退出MRU历史记录
    v           # 以只读模式打开
    /           # 在MRU列表中快速查找

####MRU vimrc配置
    let MRU_Max_Entries = 1000   # 将默认条数设为1000
    let MRU_Window_Height = 15   # 将MRU窗口高度设为15行

####推荐映射
    nmap ;f :MRU<cr>    # 按;f 打开历史记录
    nmap ;s :MRU        # 按;s 打开历史记录
    
