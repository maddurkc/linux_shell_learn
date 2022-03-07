# Basic Commands - Part02

## Command Syntax

> command [options] [arguments]

## Table of Contents

| [`shellprompt`](#shellprompt) |

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
            - but it wont persist.. display for current session only. if disconnect and it will going to replace to
                Ex:
                    $> PS1="[\t \u@\h \w>]\$"  old value
                        format: [\t \u@\h \w>]\$
                        value:
                            [18:25:04 iamadmin@localhost ~>]$ 
                            [18:25:25 iamadmin@localhost /var/log>] - if we are in /var/log folder

            - to make persist permanently(use any editor to edit, iam using vi)
                Ex:
                    $> vi .bash_profile and insert below line and save and close. reopen terminal
                        PS1="[\t \u@\h \w>]\$" 
                                OR
                        echo 'export PS1="[\t \u@\h \w>]\$"' >> ~/.bash_profile        

