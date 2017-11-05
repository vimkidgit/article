###Vim plugin of EasyMotion
 
><b>Description:</b><br>
    EasyMotion is a jump plugin. You can jump everywhere you want with  very few letter map. That's the most useful plugin I think. As showed in the figure:

![EasyMotion plugin](https://camo.githubusercontent.com/5e4ba9c43e744478405ece72de1cd285dc17079a/68747470733a2f2f662e636c6f75642e6769746875622e636f6d2f6173736574732f333739373036322f323033393631322f37636166636563382d383961352d313165332d386632632d3566323661366238336566642e676966 "EasyMotion插件")

![EasyMotion plugin](https://raw.githubusercontent.com/haya14busa/i/eab1d12a8bd322223d551956a4fd8a21d5c4bfe9/easymotion/fuzzy-incsearch-easymotion.gif "EasyMotion plugin")

![EasyMotion plugin](https://camo.githubusercontent.com/3ac76c9ea11d3b95ad5b07a24255e2fe73c131e4/68747470733a2f2f662e636c6f75642e6769746875622e636f6d2f6173736574732f333739373036322f323033393235342f34666266373237362d383939652d313165332d396266332d3165343436636162633039372e676966 "EasyMotion plugin")

><b>Download:</b><br>
    https://github.com/easymotion/vim-easymotion
[![download](https://github.com/easymotion/vim-easymotion "EasyMotion")](https://github.com/easymotion/vim-easymotion)

><b>Install:</b><br>
    Download package from github, then put the autoload,doc,plugin directory to each of the vim directory, you can also use vundle to install it.

####EasyMotion shortcut
	\\w    # find word after
    \\W    # find word before
    \\e    # find word end after
    \\E    # find word end before
    \\f	   # find letter after
    \\F	   # find letter before

####recommand vimrc map
    nmap  fw <leader><leader>w     # normal map \\w as fw 
    nmap  fW <leader><leader>W     # normal map \\W as fW
    nmap  fe <leader><leader>e     # normal map \\e as fe
    nmap  fE <leader><leader>E     # normal map \\E as fE
    nmap  a <leader><leader>f      # normal map \\f as a 
    nmap  e <leader><leader>F      # normal map \\F as e 
