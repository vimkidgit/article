####Vim file encryption

><b>Desciption</b><br>
    :X  is a command at vim command mode, it can encrypt the file to a secure way.

######Command
    :X     # encrypt file command

######Encryption
    vim test.txt  # making a new file
        test      # input your content
    :X            # input password to encrypt file
    :wq           # save and exit

######Decryption
    vim test.txt  # input password to decrypt file

######Delete the passsword
    vim test.txt  # input password decrypt the file
    :X            # input a null password

><b>Tips</b><br>
    There are have cached in NerdThree plugin, please use :wq to exit file and nerdtree, then, you can see the encrypt file.





