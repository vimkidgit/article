###Vim basic use

####Five start Command ★★★★★

#####Mode exchange ★★★★★

    esc     # to Normal mode
    i       # to Insert mode
    v       # to Visual mode
	R       # to Replace mode
    :       # to Comand mode
    /       # 查找模式

><b>Tips:About mode exchange</b><br>

    Vim mode is the first things you need to lean, a lot of person found it's mode is difficult to know, and dident know how to use vim at the begining. Vim's default mode is Normal mode. You need to press 'i' to begin edit. Why does vim edit in this way? Because in this way, you can have more control in vim. That's why vim can be the  powerful tool! So you must learn the vim mode before you edit. That's the key of the vim's door.


##### Commonly used in Normal mode ★★★★★

    k       # to go up
    j       # to go down
    h       # to go left
    l       # to go right
    u       # undo
    yy      # copy the cursor line 
    dd      # delete this line
	w       # move by word
	ctrl+d  # scroll down screen
	ctrl+u  # scroll up screen
	gg      # to the first line
	G       # to the last line
	x       # delete one letter and keep in Normal mode 
	o       # insert a line, and to go Insert mode
    p       # paste

##### Commonly used in Command mode ★★★★★

    :wq     # write and quit
    :w      # write 
    :2,10y  # copy 2 to 10 line
	:%s/hello/helloworld/g  # replace all the "hello" as "helloworld"

　
####Four start command★★★★☆

##### Commonly used in Normal mode ★★★★☆

    w       # 向后移动1个单词到词首
    b       # 向前移动1个单词到词首
    gj      # 向下移动一个位置（长行非常有用)
    gk      # 向上移动一个位置（长行非常有用)
	ctrl+e  # 向上翻一行
	ctrl+y  # 向下翻一行
	$       # 光标定位到行尾

####Three start command★★★☆☆

##### Commonly used in Normal mode ★★★☆☆
	ggvG=   # auto format the code

##### Commonly used in Command mode ★★★☆☆

    :tabnew    # open a new tab 
    :tabclose  # close the tab 
	:tabp      # to the pre tab
	:tabn      # to the next tab


><b>结语</b><br>
    有些朋友可能会觉得用个编辑器要记这么多东西实在麻烦，其实真正有用的是对于代码开发者每天经常用的人，如果文本工作少不建议使用vim	

    Many friends will found that's too many command, it's hard to remember, if you are a developer, you will always work in text file. if you always use the command, then you will remember. Practice makes perfect! Keep going.





