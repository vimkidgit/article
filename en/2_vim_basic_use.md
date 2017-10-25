###Vim basic use

####Five start Command ★★★★★

#####Mode exchange ★★★★★

    esc     # to Normal mode
    i       # to Insert mode
    v       # to Visual mode
	R       # to Replace mode
    :       # to Comand mode
    /       # to Search mode

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

    w       # move to next word ,and cursor at first letter
    b       # move to pre word, and cusor at first letter
    gj      # move down to the near next line , for the long line, it's useful 
    g       # move up to the near up line , for the long line, it's useful 
	ctrl+e  # scroll up with one line
	ctrl+y  # scroll down with one line
	$       # to the line's end

####Three start command★★★☆☆

##### Commonly used in Normal mode ★★★☆☆
	ggvG=   # auto format the code

##### Commonly used in Command mode ★★★☆☆

    :tabnew    # open a new tab 
    :tabclose  # close the tab 
	:tabp      # to the pre tab
	:tabn      # to the next tab


><b>Epilogue</b><br>

    Many friends will found that's too many command, it's hard to remember, if you are a developer, you will always work in edit text file. if you always use the command, then you will remember. Practice makes perfect! Keep going.





