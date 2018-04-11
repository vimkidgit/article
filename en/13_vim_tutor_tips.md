><b>Tips:</b><br>
    本文只是摘取vim英文文档作者认为比较有用的精华进行解读, 并不是全文详细翻译,如想看全文详细翻译,请参照vim中文文档,解读的文档版本为vim8.0. 文档位置为"vim安装目录tutor/tutor.txt"

## Vim Tutor 整理解读
><b>介绍:</b><br>
    本文对vim手册 tutor/tutor.txt (1 ~ 996 行文档解读)
    本文介绍了vim 的一个快速入教程20-30分钟入门
    本文对是该教程的一个压缩整理
    阅读本文前请先对vim的模式进行了解，主要了解插入模式(insert)和普通模式　（normal)

### 01 Lesson 1
    j       # moves down
    k       # moves up
    l       # moves right
    h       # moves left
    <ESC>   # go to normal mode
    :q!     # exits the editor
    x       # delete the charactor under the cursor
    i       # insert text 
    A       # append text
    :wq     # save a file and exit


### 02 Lesson 2
    dw      # delete a word 
    d$      # delete to the end of the line 
    w       # move the cursor one words forward
    2w      # move the cursor two words forward
    3w      # move the cursor three words forward
    0       # to move to the start of the line
    d2w     # delete two word
    dd      # delete the line
    2dd     # delete two lines
    u       # undo the last commands 
    U       # fix a whole line
    Ctrl-R  # undo the undo's 

><b>Lesson 2 Tips:</b><br>
    d [number] motion

### 03 Lesson3
    p       # put previously deleted text after the cursor 
    r       # replace the charcter
    ce      # change until the end of a word

><b>Lesson 3 Tips:</b><br>
    c [number] motion

### 04 Lesson4
    Ctrl-g  # show your location in the file and the file status
    /       # followed by a phrase to search for the phrase  
    ?       # search for a phrase in the backward direction  
    Ctrl-o  # go back to where you came from  
    Cgrl-i  # go to the latest position
    %       # find a matching ),], or }
    :s/old/new/g  # substitute 'new' for 'old' 
    :s/old/new/gc  # substitute 'new'for 'old' with confirm

### 05 Lesson 5 
    :!       # execute an external command
    :!ls     # execute an external command 'ls'
    :w TEST  # save file with filename TEST
    :!del TEST  # MS-windows removes file TEST
    :!rm  TEST  # Unix  removes file TEST
    :r TEST    # retrieves disk file TEST and puts iit below the cursor position

    
### 06 Lesson 6  
    o    # open a line below the cursor and place you in insert mode 
    O    # open a line upon  the cursor and place you in insert mode
    a    # insert text after the cursor
    R    # replace multiple charactor, press esc to exit
    y    # copy text
    p    # past
    /    # to search mode
    :set ic     # ignore case 
    :nohlsearch  # remove the hightlighting of matches
    
><b>Lesson6 Tips:</b><br>
    :set xxx    ＃ set option


### 07 Lesson 7
    ctrl+w    # jump from one windows to another
    F1        # open help file
    HELP      # open help file
    :help     # open help file
    :help w   # open help about w 
    :help c-CTRL-D   ＃open help about c-CTRL-D
	:help insert-index
	:help user-manual
    :q         # exit 
	:help cmd   # open help about cmd
    :help vimrc-intro   # open help about vimrc
    :edit ~/.vimrc		# exit vimrc file in unix
    :edit $VIM/_vimrc	# exit vimrc file in windows
    :write    # write file
    ctrl-d    # show a list of tips commands 
    TAB       # Vim will complete the name 









