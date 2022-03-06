# Basic Commands - Part01

## Table of Contents

- [man](#man)
- [who](#who)
- [whoami](#whoami)
- [uname](#uname)

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
        - pwd command to know where you are, It will print the current folder path.
            Ex: 
                $> pwd

## basename
    >
        - The basename command strips any leading directory and trailing suffix from the name.
            Ex: 
                $> basename /usr/local/
                $> basename /usr/local
        - The following example shows how to use the basename command inside a bash for loop to rename    all files ending with “.jpeg” in the current directory by replacing the file extension from “.jpeg” to “.jpg”:

                for file in *.jpeg; do
                    mv -- "$file" "$(basename $file .jpeg).jpg"
                done
