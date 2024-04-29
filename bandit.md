# bandit

## lv0 & lv0-1

* 目标：

The goal of this level is for you to log into the game using SSH. The host to which you need to connect is **bandit.labs.overthewire.org**, on port 2220. The username is **bandit0** and the password is **bandit0**. Once logged in, go to the [Level 1](https://overthewire.org/wargames/bandit/bandit1.html) page to find out how to beat Level 1.

* 命令学习：

ssh

* 解题步骤：
  
  * ssh -p 2220  [bandit0@bandit.labs.overthewire.org](mailto:bandit1@bandit.labs.overthewire.org) bandit0
  
  * ls
  
  * cat readme
  
  * 获得密码：NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

## lv1-2

- 目标：
  
  - The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

- 命令学习：
  
  - [ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)

- 解题步骤：
  
  - ssh -p 2220 bandit1@bandit.labs.overthewire.org  NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
  
  - ls
  
  - cat <-
  
  - 获得密码：rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

## lv2-3

- 目标：
  
  - The password for the next level is stored in a file called **-** located in the home directory

- 命令学习：
  
  - [ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)

- 解题步骤：
  
  - ssh -p 2220 bandit2@bandit.labs.overthewire.org rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
  
  - ls
  
  - cat 'spaces in this filename'
  
  - 获得密码: aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

## lv3-4

- 目标：
  
  - The password for the next level is stored in a hidden file in the **inhere** directory.

- 命令学习：
  
  - [ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)

- 解题步骤：
  
  - ssh -p 2220 bandit3@bandit.labs.overthewire.org aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
  
  - ls
  
  - cd inhere/
  
  - ls
  
  - cat .hidden
  
  - 获得密码：2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

## lv4-5

- 目标：
  
  - The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

- 命令学习：
  
  - [ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)

- 解题步骤：
  
  - ssh -p 2220 bandit4@bandit.labs.overthewire.org  2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
  
  - ls
  
  - cd inhere/
  
  - file ./* 或者file ./* | grep "text"
  
  - cat <-file07
  
  - 获得密码：lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

## lv5-6

- 目标：
  
  - The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:
    
    - human-readable
    - 1033 bytes in size
    - not executable

- 命令学习：
  
  - [ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)

- 解题步骤：
  
  - ssh -p 2220 [bandit5@bandit.labs.overthewire.org](mailto:bandit5@bandit.labs.overthewire.org) lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
  
  - find . -type f -size 1033c
    
    - -type 后面还有dlbcsp，用于查找指定文件类型
      
      - d：表示是一个目录（directory），事实上在ext2fs中，目录是一个特殊的文件。  
        －：表示这是一个普通的文件。  
        *
      
      - l: 表示这是一个符号链接(symbol link)文件，实际上它指向另一个文件。  
      
      - b、c：分别表示区块(block)设备和字符（character）设备，是特殊类型的文件。
      
      - s、p：这些文件关系到系统的数据结构和管道(pipe)，通常很少见到。 

    - -size 用于查找指定大小的文件
    
      - c 代表bit

- cat ./inhere/maybehere07/.file2

- 获得密码：P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

## lv6-7

- 目标：
  
  - The password for the next level is stored **somewhere on the server** and has all of the following properties:
    
    - owned by user bandit7
    - owned by group bandit6
    - 33 bytes in size

- 命令学习：
  
  - [ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html) , [grep](https://man7.org/linux/man-pages/man1/grep.1.html)

- 解题步骤：
  
  - ssh -p 2220 bandit6@bandit.labs.overthewire.org   P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
  
  - find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
    
    - 2>/dev/null把错误信息删除
    
    - 0\1\2代表标准输入、标准输出、标准错误
  
  -  cat /var/lib/dpkg/info/bandit7.password
  
  - 获得密码：z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

## lv7-8

- 目标：
  
  - The password for the next level is stored in the file **data.txt** next to the word **millionth**

- 命令学习：
  
  - [man](https://man7.org/linux/man-pages/man1/man.1.html), grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

- 解题步骤：
  
  - ssh -p 2220 bandit7@bandit.labs.overthewire.org z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
  
  - ls
  
  -  cat data.txt | grep millionth
  
  - 获得密码：millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP

## lv8-9

- 目标
  
  - The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once：

- 命令学习：
  
  - grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

- 解题步骤：
  
  - ssh -p 2220 bandit8@bandit.labs.overthewire.org TESKZC0XvTetK0S9xNwm25STk5iWrBvP
  
  - sort data.txt | uniq -u
  
  - 或者cat data.txt | sort | uniq -c | sort -n
    
    - sort -n 识别重复数据个数并按照从小到大排序
    
    - sort -rn 从大到小排序
  
  - 获得密码：EN632PlfYiZbn3PhVK3XOGSlNInNE00t

## lv9-10

- 目标：
  
  - The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

- 命令学习：
  
  - grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

- 解题步骤：
  
  - ssh -p 2220 bandit9@bandit.labs.overthewire.org EN632PlfYiZbn3PhVK3XOGSlNInNE00t
  
  - strings data.txt | grep '^='
    
    - "^正则表达式以^开头，$结尾  /$$$"
  
  - 获得密码：G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

## lv10-11

- 目标：
  
  - The password for the next level is stored in the file **data.txt**, which contains base64 encoded data

- 命令学习：
  
  - grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

- 解题步骤：
  
  - ssh -p 2220 bandit10@bandit.labs.overthewire.org G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
  
  - base64 -d data.txt
    
    - -d 解码
    
    - -i 解码时忽略非字母字符
    
    - -w 在指定的字符后换行，默认为76，0为禁止换行
    
    - --help
    
    - --version
  
  - 获得密码：The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM







- 目标：

- 命令学习：

- 解题步骤：
  
  - ssh -p 2220 bandit2 bandit.labs.overthewire.org
  
  - 获得密码：
