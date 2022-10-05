# Basic Commandline Commands in Linux:

## sudo:
    *sudo* or the *superuser* command is the most used command in linux, it lets us perform tasks which require admin/root privledges. 

    Syntax: sudo [parameters]
## pwd:
    pwd command is used to find out the path of the current working directory.
    
    Syntax: pwd [option]

    options include:
        1) -P or -physical prints the actual path of current directory.
        2) -L or -logical prints environment variable content.
## cd:
    cd is one of the most important commands, it's used to navigate between different directories on the system.

    Syntax: cd [directory_name]
            cd .. {to go back by one directory}
## cat:
    cat is one of the most frequently used comands, it's used to create a new file.

    Syntax: cat [file name] {to create a new file}
            cat [file1] [file2] > [file3] {to concatinate file1 and file2 and save them as file3}
## mv:
    It's used to move and rename file directories.

    Syntax: mv [old file name] [new file name]
## mkdir:
    mkdir is used to make a new directory.

    Syntax: mkdir [option] [directory_name]
## rmdir: 
    rmdir is used to delete an empty directory.

    Syntax: rmdir -p [directory/subdirectory]
## rm:
    rm command is used to delete files within a directory.

    Syntax: rm filename
## touch:
    touch command allows one to create an empty file.

    Syntax: touch [directory/filename]
## locate:
    locate command is used to find a file in the database.

    Syntax: locate [optional -i to make it case sensitive] [filename]
## find:
    find is used to search for a file within a specific directory.

    Syntax: find [/directory] -name [filename]
## ping:
    The ping command is used to check whether a server is available or not

    Syntax: ping [ip address or hostname]
## apt-get:
    apt-get comand is used for handling Advanced Package Tool in Ubuntu, it lets you update, intall and remove software, you need to use sudo or root privledges along with it in order for it to work 

    Syntax: apt-get [options]
