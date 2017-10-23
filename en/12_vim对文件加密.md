####vim对文件加密

><b>Desciption</b><br>
    :X  是vim下的对称加密命令,可对文件加密成二进制文件变成密文

######文件加密命令 
    :X     # 加密文件

######加密
    vim test.txt  # 新建一个文件
        test      # 输入内容
    :X            # 输入密码,加密文件
    :wq           # 保存退出

######解密
    vim test.txt  # 输入密码,解密文件

######将密码置空
    vim test.txt  # 输入密码,解密文件
    :X            # 输入空密码，即可去掉加密

><b>Tips</b><br>
    注意在NerdTree下有缓存，请:wq 退出整个文件和nerdtree,否则看不到加密文件





