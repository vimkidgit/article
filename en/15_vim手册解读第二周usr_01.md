><b>Tips:</b><br>
    These series of articles are about vim8.0 doc. I will point out some important and useful point for you. The doc files are in the vim root directory of "/doc/user_*.txt" 

## Week2
    usr_01.txt (1 ~ 192 line)

><b>Description:</b><br>
    This chapter introduces the manuals available with Vim.  Read this to know the conditions under which the commands are explained.

### 01.1 Two manuals

><b>Two manuals:</b><br>
    The Vim documentation consists of two parts:1. The User manual. Task oriented explanations, from simple to complex.  Reads from start to end like a book.  2. The Reference manual.Precise description of how everything in Vim works.
Jumping use these two commands:

    CTRL-]    # jump to a subject under the cursor
    CTRL-O    # jump back (repeat to go further back)

### 01.2 Vim installed

><b>Vimrc path:</b><br>
    An easy way to make sure you are using a nice setup is to copy the example vimrc file. It intruduce three system vimrc file config method, Unix, MS-DOS,Amiga, you can check it in the manual. here are some useful commend as below >

    :echo $VIMRUNTIME   # show vim runtime path,such as:/usr/local/share/vim/vim80
    :echo $VIM          # show vim path,such as :/usr/local/share/vim
    :set compatible?    # check if the compatible option be off
    :scriptnames        # find the script file vim loaded

### 01.3 Using the Vim tutor

><b>Vim tutor:</b><br>
     Instead of reading the text (boring!) you can use the vimtutor to learn your first Vim commands.  This is a 30 minute tutorial that teaches the most basic Vim functionality hands-on. some useful commend as below >

    vimtutor         # start vimtutor from shell
    vimtutor zh      # start vimtutor from shell with Chinese
    vimtutor fr      # start vimtutor from shell with French
    gvimtutor        # vimtutor of GUI version
    vimtutor -g      # vimtutor of GUI version

><b>Vim tutor path:</b><br>

    $VIMRUNTIME/tutor/*

><b>Vim tutor online:</b><br>
[![Vim-tutor-in-Chinese](http://www.vimkid.com/zh/14.html "Vim-tutor-in-Chinese")](http://www.vimkid.com/zh/14.html)       http://www.vimkid.com/zh/14.html  <br/>
[![Vim-tutor-in-English](http://www.vimkid.com/14.html "Vim-tutor-in-English")](http://www.vimkid.com/14.html)       http://www.vimkid.com/14.html


