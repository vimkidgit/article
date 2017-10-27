###vim plugin of NerdTree

><b>Description:</b><br>
    NerdTree is not only an directory of file, but also a goods tools to control your file. As shown in the figure

![NerdTree Plugin](http://images.vimkid.com/1_100/7_1.jpg "NerdTree Plugin")

><b>Download:</b><br>
    https://github.com/scrooloose/nerdtree
[![download](http://https://github.com/scrooloose/nerdtree "NerdTree")](https://github.com/scrooloose/nerdtree)

><b>Install:</b><br>
    First, you should download it from github. 
    Copy the autoload, doc, plugin directory's file to each of the vim root directory.

####NerdTree command shortcut
    :NERDTreeToggle<Enter>  # open or close NerdTree
    
####Commondly used shortcut in NerdTree plane
    Enter       # open in prev window
    o           # open in prev window
    x           # close parent of node
    ?           # toggle help 
    q           # quit NerdTree
    /           # search in NerdTree
    hjkl        # move
    ctrl+d      # scroll down the screen
    ctrl+u      # scroll up the screen
    u           # move tree root up a directory
    C           # change tree root ot the selected directiroy 
    r           # refresh cursor directory
    R           # refresh current root
    m           # show menu
    ma          # make a new file or directory
    mm          # remame cursor filename or directory name
    B           # bookmarks, default value if off

####Not commondly used shortcut in NerdTree plane
    go          # preview
    t           # open in new tab
    T           # open in new tab silently  
    i           # open split
    gi          # preview split
    s           # open vsplit
    gs          # preview vsplit
    X           # close all child nodes of current node recursively
    e           # explore selected directory
    P           # go to root
    p           # go to parent
    J           # go to last child
    K           # go to first child
    I           # hidden files (off)
    f           # file filters (on)

><b>Tips:NerdTree Help</b><br>
    You can also get help from NerdTree, press "?" for help. As shown in the figure.

![NerdTree help](http://images.vimkid.com/1_100/7_2.jpg "NerdTree help")

####BookMark
    :Bookmark <name>      # add the cursor node to Bookmark as name. 
    :ClearBookmarks       # clear Bookmarks
    :ClearAllBookmarks    # clear all the Bookmarks

####NerdTree vimrc config
    let NERDChristmasTree = 1    # let Nerdtree colorfuling

####Recommending vimrc map
    nmap ;j :NERDTreeToggle<cr>    # map open or close NerdTree as ;j in normal mode 
    
