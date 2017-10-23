###vim插件之EasyMotion

><b>Description:介绍</b><br>
    EasyMotion是一个跳转类插件,可以快速定位并跳转指定位置,相当值得推荐,本文只作简单常用 功能介绍详细请官方github，EasyMotion截图如下:

![EasyMotion插件](https://camo.githubusercontent.com/5e4ba9c43e744478405ece72de1cd285dc17079a/68747470733a2f2f662e636c6f75642e6769746875622e636f6d2f6173736574732f333739373036322f323033393631322f37636166636563382d383961352d313165332d386632632d3566323661366238336566642e676966 "EasyMotion插件")

![EasyMotion插件](https://raw.githubusercontent.com/haya14busa/i/eab1d12a8bd322223d551956a4fd8a21d5c4bfe9/easymotion/fuzzy-incsearch-easymotion.gif "EasyMotion插件")

![EasyMotion插件](https://camo.githubusercontent.com/3ac76c9ea11d3b95ad5b07a24255e2fe73c131e4/68747470733a2f2f662e636c6f75642e6769746875622e636f6d2f6173736574732f333739373036322f323033393235342f34666266373237362d383939652d313165332d396266332d3165343436636162633039372e676966 "EasyMotion插件")

><b>Download:官方下载地址</b><br>
    https://github.com/easymotion/vim-easymotion
[![下载地址](https://github.com/easymotion/vim-easymotion "EasyMotion")](https://github.com/easymotion/vim-easymotion)

><b>Install:安装方法</b><br>
    下载github上对应的文件
    将下载好的文件下的autoload,doc,plugin,等目录下的文件,copy到vim安装目录下的每个对应的目录下即可

####EasyMotion快捷键
	\\w    # 向后查找单词(find word after)
    \\W    # 向前查找单词(find word before)
    \\e    # 向后查找，定位到词尾(find word end after)
    \\E    # 向前查找，位位到词尾(find word end before)
    \\f	   # 向后查找单字(find letter after)
    \\F	   # 向前查找单字(find letter before)


####推荐映射 (写到vimrc 下)
    nmap  fw <leader><leader>w     # 将\\w 映射为fw 
    nmap  fW <leader><leader>W     # 将\\W 映射为fW
    nmap  fe <leader><leader>e     # 将\\e 映射为fe
    nmap  fE <leader><leader>E     # 将\\E 映射为fE
    nmap  a <leader><leader>f      # 将\\f 映射为a 
    nmap  e <leader><leader>F      # 将\\F 映射为e 
