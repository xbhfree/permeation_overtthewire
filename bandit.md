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
  
  - cat /var/lib/dpkg/info/bandit7.password
  
  - 获得密码：z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

## lv7-8

- 目标：
  
  - The password for the next level is stored in the file **data.txt** next to the word **millionth**

- 命令学习：
  
  - [man](https://man7.org/linux/man-pages/man1/man.1.html), grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

- 解题步骤：
  
  - ssh -p 2220 bandit7@bandit.labs.overthewire.org z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
  
  - ls
  
  - cat data.txt | grep millionth
  
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

## lv11-12

- 目标：
  
  - The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

- 命令学习：
  
  - grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

- 解题步骤：
  
  - ssh -p 2220 bandit11@bandit.labs.overthewire.org 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
  
  - cat data.txt | tr 'a-zA-Z' 'n-za-mN-ZA-M'
    
    - tr 转换命令，a-z转换为a->n..... z->m，即向后移动13位，是ROT13加密算法的一种实现
  
  - 获得密码：The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

## lv12-13

- 目标：
  
  - The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

- 命令学习：
  
  - grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd, mkdir, cp, mv, file

- 解题步骤：
  
  - ssh -p 2220 bandit12@bandit.labs.overthewire.org JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
  
  - mkdir /tmp/datatmp
  
  - cp data.txt /tmp/datatmp
  
  - cd /tmp/datatmp
  
  - xxd -r data.txt  > data.bin 
    
    - 16进制转换
  
  - file data.bin
  
  - mv data.bin data.gz
  
  - gzip -d data.gz
  
  - file data
  
  - mv data data.bz2
  
  - bzip2 -d data.bz2
  
  - file data
  
  - mv data data.gz
  
  - gzip -d data.gz
  
  - file data
  
  - mv data data.tar
  
  - tar xvf data.tar
  
  - file data5.bin
  
  - mv data5.bin data5.tar
  
  - tart xvf data5.tar
  
  - file data6.bin
  
  - mv data6.bin data6.bz2
  
  - bzip2 -d data6.bz2
  
  - file data6
  
  - mv data6 data6.tar
  
  - tar xvf data6.tar
  
  - file data8.bin
  
  - mv data8.bin data8.gz
  
  - gzip -d data8.gz
  
  - file data8
  
  - cat data8
  
  - 获得密码：The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
  
  - 压缩文件格式
    
    - gzip ——>  .gz       gzip -d
    
    - bzip2 ——> .bz2   bzip2 -d
    
    - tar ——> .tar        tar xvf
      
      - -x 从压缩包内提取文件
      
      - -v显示执行过程详细信息
      
      - -f指定压缩包文件

## lv13-14

- 目标：
  
  - The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. **Note:** **localhost** is a hostname that refers to the machine you are working on

- 命令学习：
  
  - ssh, telnet, nc, openssl, s_client, nmap

- 解题步骤：
  
  - ssh -p 2220 bandit13@bandit.labs.overthewire.org wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
  
  - ssh -i sshkey.private bandit14@localhost -p 2220
  
  - cat /etc/bandit_pass/bandit14
  
  - 获得密码：fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq

## lv14-15

- 目标：
  
  - The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.

- 命令学习：
  
  - ssh, telnet, nc, openssl, s_client, nmap

- 解题步骤：
  
  - ssh -p 2220 bandit14@bandit.labs.overthewire.org  fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
  
  - telnet localhost 30000
    
    - telnet命令的功能是用于控制远程主机，作为常用的telnet协议的客户端工具，使用该命令后能够控制一切开启了telnet协议支持的设备  
      原文链接：[telnet命令 &#8211; 控制远程设备 &#8211; Linux命令大全(手册)](https://www.linuxcool.com/telnet)
    
    - 语法格式：telnet [参数] 域名或IP地址  
  
  - 输入密码：fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
  
  - 获得密码：jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

## lv15-16

- 目标：
  
  - The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.
    
    **Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**

- 命令学习：
  
  - ssh, telnet, nc, openssl, s_client, nmap

- 解题步骤：
  
  - ssh -p 2220 bandit15@bandit.labs.overthewire.org jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
  
  - openssl  s_client -connect localhost:30001
    
    - openSSL是一个强大的安全套接字层密码库，囊括主要的密码算法、常用的密钥和证书封装管理功能及SSL协议，并提供丰富的应用程序供测试或其它目的使用  
      原文链接：[openssl命令 &#8211; 加密算法 &#8211; Linux命令大全(手册)](https://www.linuxcool.com/openssl)
    
    - s_client为一个SSL%2FTLS客户端程序，与s_server对应，它不仅能与s_server进行通信，也能与任何使用ssl协议的其他服务程序进行通信。
    
    - s_client -connect -host host:设置地址
    
    - s_client -connect -port:设置端口，默认443
    
    -  s_client -connec host:port 连接
    
    - 更多命令： https://blog.51cto.com/215687833/1831653
  
  - 输入密码：jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
  
  - 获得密码：JQttfApK4SeyHwDlI9SXGR50qclOAil1





























- 目标：

- 命令学习：

- 解题步骤：
  
  - ssh -p 2220 bandit2 bandit.labs.overthewire.org
  
  - 获得密码：
