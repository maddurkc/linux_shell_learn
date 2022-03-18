# Filters / Text Processor Commands

## Table of Contents

|  [`cut`](#cut)  |  [`awk`](#awk)  |  [`grep/egrep`](#grep)  |  [`sort`](#sort)  |  [`uniq`](#uniq)  |
|  [`wc`](#wc)

----

## cut

> allows you to **cut** parts of lines from specified files or piped data and print the result to standard output.
>
>it can be used to cut parts of a line by **delimiter** , **byte position** and **charecter**

<ins>***Examples:-***</ins>

* cut <<file_name>> = doesnot work. throws error. atleast you need to provide options.
    >
    Ex:-
        $> cut text_search.txt = <span style="color:red"> throws **cut: you must specify a list of bytes, characters, or fields** </span>

* cut --version or cut --help or man cut

* cut -c1 <<file_name>> = **gives 1st charecter in each line**
    >
    Ex:-
         $> cut -c1 text_search.txt

* cut -c1,3,5 <<file_name>> = **gives 1st,3rd,5th charecters in each line**
    >
    Ex:-
        $> cut -c1,3,5 text_search.txt

* cut -c1-5 <<file_name>> = **gives range of charecters in each line**
    >
    Ex:-
        $> cut -c1-5 text_search.txt

* cut -c1-2,5-9 <<file_name>> = **gives specific range of charecters in each line**
    >
    Ex:-
        $> cut -c1-3,5-9 text_search.txt

* cut -c1-2,5-9 <<file_name>> = **gives specific range of charecters in each line**
    >
    Ex:-
        $> cut -c1-3,5-9 text_search.txt

* cut -d: -f 6 <<file_name>> = **list 6th field separated by  ***':'*****
    >
    Ex:-
        $> cut -d: -f 6 /etc/passwd

* cut -d: -f 6-7 <<file_name>> = **list 6th&7th field separated by   ***':'*****
    >
    Ex:-
        $> cut -d: -f 6-7 /etc/passwd = **all users home dir . becoz 6th field is user home dir**

* ls -l | cut -c2-4 = print user permission of files/dir
    >
    Ex:-
        $> cut -d: -f 6-7 /etc/passwd = **all users home dir . becoz 6th field is user home dir**

## awk

> awk is utility designed for data extraction.

<ins>***Examples:-***</ins>

* $> awk --version   =   to check awk version
* $> awk "{print $1}" awk_lab.txt =  gives only 1st field columns data
* $> ls -l | awk '{print $1,$3}'   = list 1st and 3rd fileds of ls -l output
* $> ls -l | awk '{print $NF}'   = last filed of ls -l output
* $> awk '/Krishna/ {print}' awk_lab.txt (or) awk '/2022/ {print}' awk_lab.txt =  search for a specific word
* $> awk -F: '{print $1}' /etc/passwd = output only 1st field of /etc/passwd (delimiter : or split by : and give 1st field)
* $> echo "Hello World" | awk '{$2="krishna"; print $0}' = replace words field words
* $> awk '{$2="Maddur"; print $0}' awk_lab.txt =  same as above
* $> awk 'length($0)>20' awk_lab.txt = get lines that have morethan 20 byte size
* $> ls -l | awk '{if($9 == 'awk_lab.txt'); print $0}' - get the field matching awk_lab.txt in pwd
* $> ls -l | awk '{print NF}' or awk '{print NF}' awk_lab.txt - no of fields
