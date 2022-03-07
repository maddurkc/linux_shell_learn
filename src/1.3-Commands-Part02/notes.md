# Basic Commands - Part02

## Command Syntax

> command [options] [arguments]

## Table of Contents

| [`shellprompt`](#shellprompt) | [`aliases`](#aliases) | [`env`](#env) |

-----

## shellprompt
    > 
        Use an environment varible to customize
        - bash, ksh and sh use $PS1
        - csh, tcsh and zsh use $prompt
        Ex:
            - to check current shell prompt format 
                Ex: 
                    $> echo $PS1  
                        current format: [\u@\h \W]\$     
                        value: 
                            [iamadmin@localhost ~]$
                            [iamadmin@localhost log]$ - if we are in /var/log folder
            -  Temporary(current running session)
                Ex:
                    $> PS1="[\t \u@\h \w>]\$"  old value
                        format: [\t \u@\h \w>]\$
                        value:
                            [18:25:04 iamadmin@localhost ~>]$ 
                            [18:25:25 iamadmin@localhost /var/log>] - if we are in /var/log folder

            - to make persist permanently(use any editor to edit, iam using vi) after that run source ~/.bash_profile to reload profile
                Ex:
                    $> vi .bash_profile and insert below line and save and close
                        PS1="[\t \u@\h \w>]\$" 
                                OR
                        echo 'export PS1="[\t \u@\h \w>]\$"' >> ~/.bash_profile        

## aliases
    >  
        shrotcuts
        use for long commands
        use for commands you often type
        
        ### Temporary(current running session)
            - Viewing Alias
                Ex:
                    $> alias - displays list of alias defined.
            - Creating/Updating Aliases
                alias [name[=value]] - list or create aliases
                - use name=value to create a new alias
                Ex:
                    $> alias cls='clear' - create as alias for clear. now you can use cls instead of clear
                    $> alias lltr='ls -ltr' - now you can use lltr instead of long command as ls -ltr
            
            - Removing Aliases
                unalias name  - remove the "name" alias
                unalias -a   - remove all aliases
                Ex:
                    $> unalias cls - will remove cls alias we created earlier

         ### Persisting Aliases
            - add aliases to your personal initialization files(.bash_profile)

            Ex:- vi ~/.bash_profile and insert below lines after that run source ~/.bash_profile to reload profile
                alias lltr="ls -ltr"
                alias cls="clear"

## env
    >  
        name/value pair

        ### Temporary(current running session)
            - Viwewing environment varible
                Syntax: printenv [environment varible name]    
                    Ex:
                        $> env or printenv  - displays list of environment varible defined
                        $> printenv PWD or echo $PWD - display value for environment variable PWD

            - creating/updating environment varible 
                Syntax: export <<varible_name>>="<<value>>"
                    Ex:
                        $> export EDITOR="vi"
                        $> export TZ="US/Pacific"

            - removing environment varible 
                Syntax: unset <<varible_name>>
                    Ex:
                        $> unset TZ
        
        ### Persisting environment varible
            - add environment variabled to your personal initialization files(.bash_profile)

            Ex:- vi ~/.bash_profile and insert below lines after that run source ~/.bash_profile to reload profile
                 export EDITOR = "vi"