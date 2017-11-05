###Vim plugin of MRU

><b>Description:</b><br>
    MRU is a classic plugin. It had been created for many years. This plugin can open the file you had ever opened in a very fast way. 

![MRU](http://images.vimkid.com/1_100/3_1.jpg "MRU")

><b>Download:</b><br>
    http://www.vim.org/scripts/script.php?script_id=521 
[![Download](http://www.vim.org/scripts/script.php?script_id=521 "MRU")](http://www.vim.org/scripts/script.php?script_id=521)

><b>Install:</b><br>
    Download `mru.vim` , and put it at the vim's `plugin` directory, or you can use vundle to install it.

####MRU command
    :MRU <Enter>        # open MRU file list.
    :MRU pattern<tab>   # open MRU file with search
    
####MRU shortcuts
    j           # move up in the MRU file list
    k           # move down in the MRU file list
    Enter       # open file in the cursor at this tag
    t           # open file in the cursor with a new tag
    u           # update MRU file list
    q           # exit MRU file list
    v           # open with readonly mode
    /           # search in MRU file list

####MRU vimrc config
    let MRU_Max_Entries = 1000   # set the record lines  as 1000 in MRU file list
    let MRU_Window_Height = 15   # set the MRU height as 15 lines

####MRU maps in vimrc
    nmap ;f :MRU<cr>    # map open MRU as ;f in normal mode
    nmap ;s :MRU        # nap open MRU as ;s and keep in command mode
    
