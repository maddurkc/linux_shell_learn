# Basic Commands - Part01

## Table of Contents

- [man](#man)
- [who](#man)
- [whoami](#man)
- [uname](#man)

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
