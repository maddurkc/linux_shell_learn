# Basic Commands - Part01

## Command Syntax

> command [options] [arguments]

## Table of Contents

- [man](#man)
- [who](#who)
- [whoami](#whoami)
- [uname](#uname)
- [pwd](#pwd)
- [basename](#basename)
- [history](#history)
- [env](#env)
- [ls](#ls)
- [mkdir](#mkdir)
- [cd](#cd)
- [cp](#cp)
- [mv](#mv)
- [rm](#rm)

| [man](#man) | [who](#who) | [whoami](#whoami) | [uname](#uname) | [pwd](#pwd) | [basename](#basename) |
| [history](#history) | [env](#env) | [ls](#ls) | [mkdir](#mkdir) | [cd](#cd) | [cp](#cp) |
| [mv](#mv) | [rm](#rm) |

-----

## man
    > 
        I don't know how to use a command, I type man <command_name> to get manual of the command
            Ex:
                $> man ls
                $> man cat

## who
    > 
        - The who command displays the users logged in to the system.
            Ex:
                $> who
        - -aH flags will tell who to display more information, including the idle time and the process ID
            Ex:
                $> who -aH

## whoami
    >
        - whoami to print the user name currently logged in to the terminal session
            Ex:
                $> whoami

## uname
    >
        - uname without any options will return the Operating System codename
            Ex: 
                $> uname

        - The a option prints all the information
            Ex: 
                $> uname -a

        - The s option prints the Operating System name. r prints the release, v prints the version
            Ex: 
                $> uname -srv

        - The a option prints all the information
            Ex: 
                $> uname -a

## pwd
    >
        - pwd command to know where you are, It will print the current folder path(full path).
            Ex: 
                $> pwd

## basename
    >
        - The basename command strips any leading directory and trailing suffix from the name.
            Ex: 
                $> basename /usr/local/
                $> basename /usr/local

        - The below example shows how to use the basename command inside a bash for loop to rename   
        all files ending with “.jpeg” in the current directory by replacing the file extension
        from “.jpeg” to “.jpg”:

                for file in *.jpeg; do
                    mv -- "$file" "$(basename $file .jpeg).jpg"
                done

## history
    >
        -  inside .bash_history file

        - Every time we run a command, that's memorized in the history, This shows the history with numbers
            Ex: 
                $> history

        - The c option is used to clear the history. 
            Ex: 
                $> history -c

        - You can combine this with grep to find a command you ran:
            Ex: 
                $> history | grep uname

## ls

    > Inside a folder you can list all the files that the folder contains
            Ex:
                $> ls - current location listing
                $> ls /bin - bin folder listing
                $> ls -l - long listing
                $> ls -1 - each file name with new line
                $> l. - hidden files
                $> ls -a - display all file names including hidden files 

## mkdir

    > You create folders using the mkdir
            Ex:
                $> mkdir fruits - will create folder in current directory
                $> mkdir dogs cars - create multiple folders
                $> mkdir -p fruits/apples - create multiple nested folders
                $> mkdir ~/fruits - will create folder in user home directory as mentioned

## cd

    > you can move into a folder. cd means change directory
            Ex:
                $> cd fruits - will move into fruits folder
                $> cd .. - one folder back
                $> cd . - nothing happen. it will stay into current folder
                $> cd /etc - using this absolute path starts from root folder and move into etc folder
                $> cd ../fruits - it will go one folder back and move to mentioned folder here fruits

## cp

    > 

## mv

    >

## rm

    >
