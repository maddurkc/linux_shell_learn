# File Display Commands

## Table of Contents

|  [`cat`](#cat) |  [`more`](#more) |  [`less`](#less) |  [`head`](#head) |  [`tail`](#tail)

----

## cat

> **cat** command will displays the file content(scrolled to last page) and also add content to a file

<ins>***Examples:-***</ins>

* cat <<file_name>> = **print a file's content to the standard output**
    >
    Ex:-
        $> cat messages

* cat <<file_name1>> <<file_name2>> = **print the content of multiple files**
    >
    Ex:-
        $> cat awk_lab.txt text_search.txt

* cat <<file_name1>> <<file_name2>>  > <<file_name3>>= **using the output redirection operator > you can concatenate the content of multiple files into a new file**
    >
    Ex:-
        $> cat awk_lab.txt text_search.txt > merge_awk_text_search.txt

* cat <<file_name1>> <<file_name2>>  >> <<file_name3>>= **Using >> you can append the content of multiple files into a new file, creating it if it does not exist**
    >
    Ex:-
        $> cat awk_lab.txt text_search.txt >> merge_awk_text_search.txt

* cat -n <<file_name>>= **print's file content along with line numbers for even empty lines also**
    >
    Ex:-
        $> cat -n text_search.txt

* cat -nb <<file_name>>= **remove line numbers for all the empty lines**
    >
    Ex:-
        $> cat -nb text_search.txt

> ***Note:-***
> ***cat is often used in combination with the pipe operator | to feed a file content as input to another command: cat file1 | anothercommand***

## more

> **more** command will displays the file content one page at a time in case the file is large (For example log files)
>
> **more** command also allows the user do scroll up and down through the page.
>
> ###  While viewing the text file use these controls

| Key    | Meaning                              |
| :---:  | :---                                 |
| Enter  |  to scroll down page line by line    |
| Space  |  to go to next page                  |
|  b     |  to go to the backward page          |
|  /     |  lets you search the string          |
>
> ### more options

| Options            | Function                                             |
| :---               | :---                                                 |
| more -num          |  Limits the line displayed per page.                 |
| more -d            |  Displays user message at right corner.              |
| more -s            |  Squeeze blank lines.                                |
| more +/string name |  It helps to find the string.                        |
| more +num name     |  Used to display the content from a specific line.   |


<ins>***Examples:-***</ins>

* more <<file_name>> = **print a file's content one page at a time to the standard output**
    >
    Ex:-
        $> more messages

* more -d <<file_name>> = **Use this command in order to help the user to navigate. It displays “[Press space to continue, ‘q’ to quit.]”**
    >
    Ex:-
        $> more -d messages

> ***Note:-***
> ***'more' command can't be used to display binary files.***
