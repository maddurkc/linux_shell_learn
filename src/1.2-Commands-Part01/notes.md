# Basic Commands - Part01

## Table of Contents

- [man](#man)
- [who](#who)
- [whoami](#whoami)
- [uname](#uname)
- [pwd](#pwd)
- [basename](#basename)
- [history](#history)
- [env](#env)

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

## env
    >
