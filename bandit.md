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
    
    - s_client -connec host:port 连接
    
    - 更多命令： https://blog.51cto.com/215687833/1831653
  
  - 输入密码：jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
  
  - 获得密码：JQttfApK4SeyHwDlI9SXGR50qclOAil1

## lv16-17

- 目标：
  
  - The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

- 命令学习：
  
  - ssh, telnet, nc, openssl, s_client, nmap
  
  - nmap
    
    * 扫描指定端口
    - nmap -p [地址或者地址范围]  域名
  
  - chmod
    
    - chmod abc file
    
    - a,b,c各为一个数字，分别表示User、Group、及Other的权限
    
    - r、w、x、代表读、写、执行——r=4，w=2，x=1

- 解题步骤：
  
  - ssh -p 2220 bandit16@bandit.labs.overthewire.org JQttfApK4SeyHwDlI9SXGR50qclOAil1
  
  - nmap -p 31000-32000 localhost
  
  - 获得
    
    - 31046/tcp open  unknown
      31518/tcp open  unknown
      31691/tcp open  unknown
      31790/tcp open  unknown
      31960/tcp open  unknown
  
  - openssl s_client -connect localhost:31046
    
    - dopenssl s_client -connect localhost:31518
    
    - openssl s_client -connect localhost:31691
    
    - openssl s_client -connect localhost:31790 正确
    
    - openssl s_client -connect localhost:31960
  
  - 获得ssh.pirvate 
    
    - ```textile
      -----BEGIN RSA PRIVATE KEY-----
      MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
      imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
      Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
      DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
      JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
      x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
      KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
      J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
      d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
      YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
      vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
      +TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
      8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
      SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
      HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
      SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
      R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
      Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
      R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
      L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
      blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
      YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
      77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
      dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
      vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
      -----END RSA PRIVATE KEY-----
      ```
  
  - vim /tmp/bandit16/key 将上述令牌放入key中
  
  - cd /tmp/bandit16/
  
  - ssh -i key bandit17@localhost -p 2220
  
  - 权限不够
  
  - touch key
    
    - vim编辑模式下通过Esc键进入命令模式  
      输入:set paste设置粘贴状态  
      通过输入‘i’重新进入编辑模式，进行粘贴操作  
      粘贴完成后执行:set nopaste 即可取消粘贴状态设置
      
      无效
  
  - vim -c  'set nocompatible'  -c 'set vbs=:verbatim' key
  
  - chmod 400 key
  
  - ssh -i key bandit17@localhost -p 2220
  
  - cat /etc/bandit_pass/bandit17
  
  - 获得密码：VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e

## lv17-18

- 目标：
  
  - There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**
    
    **NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19**

- 命令学习：
  
  - cat, grep, ls, diff
  
  - diff
    
    - diff 参数 文件名1 文件名2  
      原文链接：[diff命令 &#8211; 比较文件内容差异 &#8211; Linux命令大全(手册)](https://www.linuxcool.com/diff)

- 解题步骤：
  
  - ssh -p 2220 bandit17@bandit.labs.overthewire.org VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
  
  - diff passwords.old  passwords.new
  
  - 42c42
    < p6ggwdNHncnmCNxuAt0KtKVq185ZU7AW
    
    ---
    
    > hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
  
  - 获得密码：hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg

## lv18-19

- 目标：
  
  - The password for the next level is stored in a file **readme** in the homedirectory. Unfortunately, someone has modified **.bashrc** to log you out when you log in with SSH.

- 命令学习：
  
  - ssh, ls, cat

- 解题步骤：
  
  - ssh -p 2220 bandit18@bandit.labs.overthewire.org “cat ./readme"   hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
  
  - 获得密码：awhqfNnAbc1naukrpqDYcF95h7HoMTrC

## lv19-20

- 目标：
  
  - To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

- 命令学习：
  
  - [setuid on Wikipedia](https://en.wikipedia.org/wiki/Setuid)

- 解题步骤：
  
  - ssh -p 2220 bandit19@bandit.labs.overthewire.org awhqfNnAbc1naukrpqDYcF95h7HoMTrC
  
  - ls -la 发现bandit20-do 有执行权限
  
  - ./bandit20-do cat /etc/bandit_pass/bandit20  用bandit20-do获取权限，查看密码
  
  - 获得密码：VxCazJaVykI6W36BkBU0mJTCM8rR95XT

## lv20-21

- 目标：
  
  - There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).
    
    **NOTE:** Try connecting to your own network daemon to see if it works as you think

- 命令学习：
  
  - ssh, nc, cat, bash, screen, tmux, Unix ‘job control’ (bg, fg, jobs, &, CTRL-Z, …)
  
  - nc命令来自英文词组net cat的缩写，其功能是扫描与连接指定端口。  
    原文链接：[nc命令 &#8211; 扫描与连接指定端口 &#8211; Linux命令大全(手册)](https://www.linuxcool.com/nc)
    
    - 语法格式：nc 参数 域名或IP地址  
    
    - -l 监听模式
    
    - -p 设置本地主机使用的端口
    
    - -v 显示执行过程
    
    - -h 显示帮助信息

- 解题步骤：
  
  - ssh -p 2220 bandit20@bandit.labs.overthewire.org VxCazJaVykI6W36BkBU0mJTCM8rR95XT
  
  - printf "VxCazJaVykI6W36BkBU0mJTCM8rR95XT" | nc -l -p 7777 &
    
    - printf 可以用 echo代替
    
    - 或者 nc -l 2333 < /etc/bandit_pass/bandit20 & 用上一关得知的密码文件
    
    - & 起到后台运行的作用
    
    - 端口7777为随意指定的空闲端口
  
  - ./suconnect 7777
  
  - 获得密码：NvEJF7oVjkddltPSrdKEFOllh9V1IBcq

## lv21-22

- 目标：
  
  - A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

- 命令学习：
  
  - cron, crontab, crontab(5) (use “man 5 crontab” to access this)

- 解题步骤：
  
  - ssh -p 2220 bandit21@bandit.labs.overthewire.org NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
  
  - ls
  
  - cat cronjob_bandit22
    
    - 获得：@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
      
      * * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
  
  - cat  /usr/bin/cronjob_bandit22.sh
    
    - #!/bin/bash
      chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
      cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
  
  - cat  /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
  
  - 获得密码：WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff

## lv22-23

- 目标：
  
  - A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.
    
    **NOTE:** Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

- 命令学习：
  
  - cron, crontab, crontab(5) (use “man 5 crontab” to access this)
  
  - crontab
    
    - crontab命令来自英文词组cron table的缩写，其功能是管理定时计划任务  
      原文链接：[crontab命令 &#8211; 管理定时计划任务 &#8211; Linux命令大全(手册)](https://www.linuxcool.com/crontab)
  
  - cut
    
    - cut命令的功能是按列提取文件内容。  
    
    - -d 设置分隔符
    
    - -f 显示指定字段内容
    
    - --help

- 解题步骤：
  
  - ssh -p 2220 bandit22@bandit.labs.overthewire.org WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff
  
  - cd /etc/cron.d
  
  - cat cronjob_bandit23
    
    - @reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
      
      * * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
  
  - cat  /usr/bin/cronjob_bandit23.sh
    
    - ```bash
      #!/bin/bash
      
      myname=$(whoami)
      mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)
      
      echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"
      
      cat /etc/bandit_pass/$myname > /tmp/$mytarget
      ```
  
  - echo I am user bandit23 | md5sum | cut -d ' ' -f 1
    
    - 8ca319486bfbbc3663ea0fbe81326349
  
  - cat /tmp/8ca319486bfbbc3663ea0fbe81326349
  
  - 获得密码：QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G

## lv23-24

- 目标：
  
  - A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.
    
    **NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!
    
    **NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

- 命令学习：
  
  - cron, crontab, crontab(5) (use “man 5 crontab” to access this)
  
  - timeout
    
    - 使用 `SIGKILL` 可能会导致数据丢失或其他未预期的副作用，因为进程在接收到 `SIGKILL` 时不会有任何机会进行清理。在大多数情况下，使用 `SIGTERM`（默认信号，编号为 15）会更安全，因为它允许进程在终止前进行清理。如果你想要使用 `SIGTERM`，可以简单地省略 `-s 9` 部分，或者明确地使用 `-s 15`

- 解题步骤：
  
  - ssh -p 2220 bandit23@bandit.labs.overthewire.org QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
  
  - cd /etc/cron.d
  
  - cat cronjob_bandit24
  
  - cat  /usr/bin/cronjob_bandit24.sh
    
    - ```bash
      #!/bin/bash
      
      myname=$(whoami)
      
      cd /var/spool/$myname/foo
      echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
      for i in * .*;
      do
         if [ "$i" != "." -a "$i" != ".." ];
         then
             echo "Handling $i"
             owner="$(stat --format "%U" ./$i)"
             if [ "${owner}" = "bandit23" ]; then
                 timeout -s 9 60 ./$i
             fi
             rm -f ./$i
         fi
      done
      ```
    
    - 复制到bandit24，myname等于bandit24，判断如果owner等于bandit23，执行shell命令，60秒不成功就报9错误，然后删除下面的所有文件
  
  - cd /tmp/bandit23/
  
  - vim shell.sh
    
    - ```vim
      #!/bin/bash
      cat /etc/bandit_pass/bandit24 >> /tmp/bandit23/bandit23pass
      ```
  
  - chmod 777 shell.sh
  
  - cp shell.sh /var/spool/bandit24/foo/
  
  - 获得密码：VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar

## lv24-25

- 目标：
  
  - A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.  
    You do not need to create new connections each time

- 命令学习：
  
  - nc
    
    - nc 参数 域名或IP地址  
      原文链接：[nc命令 &#8211; 扫描与连接指定端口 &#8211; Linux命令大全(手册)](https://www.linuxcool.com/nc)

- 解题步骤：
  
  - ssh -p 2220 bandit24@bandit.labs.overthewire.org VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
  
  - mkdir /tmp/bandit24tmp
  
  - cd /tmp/bandit24tmp
  
  - vim shell.sh
    
    - ```vim
      for ((i=1000;i<10000;i++));do echo "VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i" >> pingcode.txt;done
      
      ### nc localhost -p 30002 < pingcode.txt
      
      cat ./pingcode.txt | nc localhost -p 30002 >> ./bandit24pass
      echo -e ./pingcode.txt | nc localhost -p 30002 >> ./bandit24pass
      echo -e "$BANDIT24_PASS $PIN" | nc localhost 30002 >> ./bandit242pass
      
      #!/bin/bash  
      
      # 假设你已经有了bandit24的密码  
      BANDIT24_PASS="VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar"  
      
      # 尝试从0000到9999的所有PIN码  
      for PIN in {0000..9999}  
      do  
          # 使用netcat与守护进程通信  
          # 注意：这取决于守护进程的具体行为，可能需要调整  
          RESPONSE=$(echo -e "$BANDIT24_PASS $PIN" | nc localhost 30002)  
      
          # 检查响应中是否包含"correct"或类似的消息  
          if [[ $RESPONSE == *"orrect"* ]]; then  
              echo "Found the PIN: $PIN"  
              echo "The response from the daemon is: $RESPONSE"  
              # 这里可以添加逻辑来提取并打印bandit25的密码（如果它在响应中）  
              break  # 退出循环  
          fi  
      done
      
      
      
      
      from pwn import *
      
      conn = remote('localhost', '30002')
      badline = conn.recvline()
      for i in range(10000):
          tmp = str(i).zfill(4)
          print ('[+] Trying pincode: ' + str(tmp))
          conn.sendline('VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar ' + tmp)
          response = conn.recvline()
          print(response)
          if b'Wrong! Please enter the correct pincode. Try again.' not in response:
              print('[+] Found pincode: ' + str(tmp))
               break
      
      
       for i in {0000..9999};do echo VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i;done | nc localhost 30002
      
      
      
      
      #!/bin/bash  
      
      # 假设你已经有了bandit24的密码  
      BANDIT24_PASS="VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar"  
      
      # 尝试从0000到9999的所有PIN码  
      for PIN in {0000..9999}  
      do  
          # 使用netcat与守护进程通信  
          # 注意：这取决于守护进程的具体行为，可能需要调整  
          RESPONSE=$(echo "$BANDIT24_PASS $PIN" | nc localhost 30002)  
      
          # 检查响应中是否包含"correct"或类似的消息  
          if [[ $RESPONSE == *"orrect"* || $PIN%500 == 0]]; then  
              echo "Found the PIN: $PIN"  
              echo "The response from the daemon is: $RESPONSE"
              sleep 2  
              # 这里可以添加逻辑来提取并打印bandit25的密码（如果它在响应中）  
              break  # 退出循环  
          fi  
      done
      
      
      
      
      echo VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar 0000 | nc localhost 30002
      printf VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar 0000 | nc localhost 30002
      
      
      str="Hello, abc is here."  
      if [[ "$str" =~ abc ]]; then  
          echo "String contains 'abc'."  
      else  
          echo "String does not contain 'abc'."  
      fi
      
      
      str="Hello, abc is here."  
      if echo "$str" | grep -q "abc"; then  
          echo "String contains 'abc'."  
      else  
          echo "String does not contain 'abc'."  
      fi
      ```

      from pwn import *
    
      r = remote('localhost', 30002)
      for i in range(0, 10):
          for j in range(0, 10):
              for k in range(0, 10):
                  for p in range(0, 10):
                      flag = str(i) + str(j) + str(k) + str(p)
                      s = "VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar "+ flag
                      r.sendline(s)
                      response = r.recvline()
                      if 'Wrong!' not in response:
                          print 'Correct! ' + responsee
    
      ```

- ./shell.sh

- 获得密码：

# 模板

- 目标：

- 命令学习：

- 解题步骤：
  
  - ssh -p 2220 bandit2 bandit.labs.overthewire.org
  
  - 获得密码：
