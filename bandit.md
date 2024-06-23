# bandit

## lv0 & lv0-1

* 目标：

The goal of this level is for you to log into the game using SSH. The host to which you need to connect is **bandit.labs.overthewire.org**, on port 2220. The username is **bandit0** and the password is **bandit0**. Once logged in, go to the [Level 1](https://overthewire.org/wargames/bandit/bandit1.html) page to find out how to beat Level 1.

* 命令学习：

ssh

* 解题步骤：
  
  * ssh -p 2220  bandit0@bandit.labs.overthewire.org 
    * bandit0
  
  * ls
  
  * cat readme
  
  * 获得密码：ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

## lv1-2

- 目标：
  
  - The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

- 命令学习：
  
  - [ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)

- 解题步骤：
  
  - ssh -p 2220 bandit1@bandit.labs.overthewire.org  
    - ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
  
  - ls
  
  - cat <-
  
  - 获得密码：263JGJPfgU6LtdEvgfWU1XP5yac29mFx

## lv2-3

- 目标：
  
  - The password for the next level is stored in a file called **-** located in the home directory

- 命令学习：
  
  - [ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)

- 解题步骤：
  
  - ssh -p 2220 bandit2@bandit.labs.overthewire.org 
    - ​	
  
  - ls
  
  - cat 'spaces in this filename'
  
  - 获得密码: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

## lv3-4

- 目标：
  
  - The password for the next level is stored in a hidden file in the **inhere** directory.

- 命令学习：
  
  - [ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)

- 解题步骤：
  
  - ssh -p 2220 bandit3@bandit.labs.overthewire.org 
    - MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
  
  - ls
  
  - cd inhere/
  
  - ls
  
  -  cat ./...Hiding-From-You
  
  - 获得密码：2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

## lv4-5

- 目标：
  
  - The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

- 命令学习：
  
  - [ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)

- 解题步骤：
  
  - ssh -p 2220 bandit4@bandit.labs.overthewire.org  
    - 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
  
  - ls
  
  - cd inhere/
  
  - file ./* 或者file ./* | grep "text"
  
  - cat <-file07
  
  - 获得密码：4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

## lv5-6

- 目标：
  
  - The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:
    
    - human-readable
    - 1033 bytes in size
    - not executable

- 命令学习：
  
  - [ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)

- 解题步骤：
  
  - ssh -p 2220 bandit5@bandit.labs.overthewire.org 
    - 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
  
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

- 获得密码：HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

## lv6-7

- 目标：
  
  - The password for the next level is stored **somewhere on the server** and has all of the following properties:
    
    - owned by user bandit7
    - owned by group bandit6
    - 33 bytes in size

- 命令学习：
  
  - [ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html) , [grep](https://man7.org/linux/man-pages/man1/grep.1.html)

- 解题步骤：
  
  - ssh -p 2220 bandit6@bandit.labs.overthewire.org   
    - HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
  
  - find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
  
    - 2>/dev/null把错误信息删除
  
    - 0\1\2代表标准输入、标准输出、标准错误
  
  - cat /var/lib/dpkg/info/bandit7.password
  
  - 获得密码：morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

## lv7-8

- 目标：
  
  - The password for the next level is stored in the file **data.txt** next to the word **millionth**

- 命令学习：
  
  - [man](https://man7.org/linux/man-pages/man1/man.1.html), grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

- 解题步骤：
  
  - ssh -p 2220 bandit7@bandit.labs.overthewire.org 
    - morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
  
  - ls
  
  - cat data.txt | grep millionth
  
  - 获得密码：millionth       dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

## lv8-9

- 目标
  
  - The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once：

- 命令学习：
  
  - grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

- 解题步骤：
  
  - ssh -p 2220 bandit8@bandit.labs.overthewire.org 
    - dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
  
  - sort data.txt | uniq -u
  
  - 或者cat data.txt | sort | uniq -c | sort -n
  
    - sort -n 识别重复数据个数并按照从小到大排序
  
    - sort -rn 从大到小排序
  
  - 获得密码：4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

## lv9-10

- 目标：
  
  - The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

- 命令学习：
  
  - grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

- 解题步骤：
  
  - ssh -p 2220 bandit9@bandit.labs.overthewire.org 
    - 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
  
  - strings data.txt | grep '^='
  
    - "^正则表达式以^开头，$结尾  /$$$"
  
  - 获得密码：FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

## lv10-11

- 目标：
  
  - The password for the next level is stored in the file **data.txt**, which contains base64 encoded data

- 命令学习：
  
  - grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

- 解题步骤：
  
  - ssh -p 2220 bandit10@bandit.labs.overthewire.org 
    - FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
  
  - base64 -d data.txt
  
    - -d 解码
  
    - -i 解码时忽略非字母字符
  
    - -w 在指定的字符后换行，默认为76，0为禁止换行
  
    - --help
  
    - --version
  
  - 获得密码：The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

## lv11-12

- 目标：
  
  - The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

- 命令学习：
  
  - grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

- 解题步骤：
  
  - ssh -p 2220 bandit11@bandit.labs.overthewire.org 
    - dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
  
  - cat data.txt | tr 'a-zA-Z' 'n-za-mN-ZA-M'
  
    - tr 转换命令，a-z转换为a->n..... z->m，即向后移动13位，是ROT13加密算法的一种实现
  
  - 获得密码：The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

## lv12-13

- 目标：
  
  - The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

- 命令学习：
  
  - grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd, mkdir, cp, mv, file

- 解题步骤：
  
  - ssh -p 2220 bandit12@bandit.labs.overthewire.org 
    - 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
  
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
  
  - tar xvf data5.tar
  
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
  
  - 获得密码：The password is FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
  
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
  
  - ssh -p 2220 bandit13@bandit.labs.overthewire.org 
    - FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
  
  - ssh -i sshkey.private bandit14@localhost -p 2220
  
  - cat /etc/bandit_pass/bandit14
  
  - 获得密码：MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS

## lv14-15

- 目标：
  
  - The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.

- 命令学习：
  
  - ssh, telnet, nc, openssl, s_client, nmap

- 解题步骤：
  
  - ssh -p 2220 bandit14@bandit.labs.overthewire.org  
    - MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
  
  - telnet localhost 30000
  
    - telnet命令的功能是用于控制远程主机，作为常用的telnet协议的客户端工具，使用该命令后能够控制一切开启了telnet协议支持的设备  
      原文链接：[telnet命令 &#8211; 控制远程设备 &#8211; Linux命令大全(手册)](https://www.linuxcool.com/telnet)
  
    - 语法格式：telnet [参数] 域名或IP地址  
  
  - 输入密码：MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
  
  - 获得密码：8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo

## lv15-16

- 目标：
  
  - The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.
    
    **Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**

- 命令学习：
  
  - ssh, telnet, nc, openssl, s_client, nmap

- 解题步骤：
  
  - ssh -p 2220 bandit15@bandit.labs.overthewire.org 
    - 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
  
  - openssl  s_client -connect localhost:30001
  
    - openSSL是一个强大的安全套接字层密码库，囊括主要的密码算法、常用的密钥和证书封装管理功能及SSL协议，并提供丰富的应用程序供测试或其它目的使用  
      原文链接：[openssl命令 &#8211; 加密算法 &#8211; Linux命令大全(手册)](https://www.linuxcool.com/openssl)
  
    - s_client为一个SSL%2FTLS客户端程序，与s_server对应，它不仅能与s_server进行通信，也能与任何使用ssl协议的其他服务程序进行通信。
  
    - s_client -connect -host host:设置地址
  
    - s_client -connect -port:设置端口，默认443
  
    - s_client -connec host:port 连接
  
    - 更多命令： https://blog.51cto.com/215687833/1831653
  
  - 输入密码：8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
  
  - 获得密码：kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

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
  
  - ssh -p 2220 bandit16@bandit.labs.overthewire.org 
  
    - kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
  
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
  
  - 获得密码：EReVavePLFHtFlFsjn3hyzMlvSuSAcRD

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
  
  - ssh -p 2220 bandit17@bandit.labs.overthewire.org 
  
    - EReVavePLFHtFlFsjn3hyzMlvSuSAcRD
  
  - diff passwords.old  passwords.new
  
  - 42c42
    < p6ggwdNHncnmCNxuAt0KtKVq185ZU7AW
  
    ---
  
    > x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
  
  - 获得密码：x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO

## lv18-19

- 目标：
  
  - The password for the next level is stored in a file **readme** in the homedirectory. Unfortunately, someone has modified **.bashrc** to log you out when you log in with SSH.

- 命令学习：
  
  - ssh, ls, cat

- 解题步骤：
  
  - ssh -p 2220 bandit18@bandit.labs.overthewire.org “cat ./readme"   
    - x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
  
  - 获得密码：cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8

## lv19-20

- 目标：
  
  - To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

- 命令学习：
  
  - [setuid on Wikipedia](https://en.wikipedia.org/wiki/Setuid)

- 解题步骤：
  
  - ssh -p 2220 bandit19@bandit.labs.overthewire.org 
    - cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8
  
  - ls -la 发现bandit20-do 有执行权限
  
  - ./bandit20-do cat /etc/bandit_pass/bandit20  用bandit20-do获取权限，查看密码
  
  - 获得密码：0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO

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
  
  - ssh -p 2220 bandit20@bandit.labs.overthewire.org 
    - 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
  
  - printf "0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO" | nc -l -p 7777 &
  
    - printf 可以用 echo代替
  
    - 或者 nc -l 2333 < /etc/bandit_pass/bandit20 & 用上一关得知的密码文件
  
    - & 起到后台运行的作用
  
    - 端口7777为随意指定的空闲端口
  
  - ./suconnect 7777
  
  - 获得密码：EeoULMCra2q0dSkYj561DX7s1CpBuOBt

## lv21-22

- 目标：
  
  - A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

- 命令学习：
  
  - cron, crontab, crontab(5) (use “man 5 crontab” to access this)

- 解题步骤：
  
  - ssh -p 2220 bandit21@bandit.labs.overthewire.org 
    - EeoULMCra2q0dSkYj561DX7s1CpBuOBt
  
  - ls
  
  - cat cronjob_bandit22
  
    - 获得：@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
      
      * * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
  
  - cat  /usr/bin/cronjob_bandit22.sh
  
    - #!/bin/bash
      chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
      cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
  
  - cat  /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
  
  - 获得密码：tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q

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
  
  - ssh -p 2220 bandit22@bandit.labs.overthewire.org 
  
    - tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q
  
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
  
  - 获得密码：0Zf11ioIjMVN551jX3CmStKLYqjk54Ga

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
  
  - ssh -p 2220 bandit23@bandit.labs.overthewire.org 
  
    - 0Zf11ioIjMVN551jX3CmStKLYqjk54Ga
  
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
  
  - cat bandit23pass
  
  - 获得密码：gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8

## lv24-25[尚有问题]

- 目标：
  
  - A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.  
    You do not need to create new connections each time

- 命令学习：
  
  - nc
    
    - nc 参数 域名或IP地址  
      原文链接：[nc命令 &#8211; 扫描与连接指定端口 &#8211; Linux命令大全(手册)](https://www.linuxcool.com/nc)

- 解题步骤：
  
  - ssh -p 2220 bandit24@bandit.labs.overthewire.org 
  
    - gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8
  
  - mkdir /tmp/bandit24tmp
  
  - cd /tmp/bandit24tmp
  
  - vim shell.sh
  
    - ```shell
      for ((i=1000;i<10000;i++));do echo "VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i" >> pingcode.txt;done
      
      #!/bin/bash  
      BANDIT24_PASS="VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar"  
      
      for PIN in {0000..9999}  
      do  
          RESPONSE=$(echo "$BANDIT24_PASS $PIN" | nc localhost 30002)  
          if [[ $RESPONSE == *"Correct"* ]]  
          then  
              echo "Found the PIN: $PIN"  
              echo "The response from the daemon is: $RESPONSE"  
              break  
          elif [[ $RESPONSE == *"Wrong"* ]]  # 假设响应中可能包含 "Wrong"  
          then  
              echo "The PIN $PIN is wrong."  
          fi  
      
          # 每1000次迭代后暂停2秒（注意：是从0开始计数的，所以应该是 % 1000 == 0）  
          if (( $PIN % 1000 == 0 )); then  
              sleep 2  
          fi  
      done
      ```
  
- ```a.sh
  -----实际可行 创建两个sh文件，拆开查询
  #!/bin/bash 
  BANDIT24_PASS="gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8"  
  set t 1
  for PIN in {0000..9999}  
  do  
     if (( $PIN % 500 == 0 )); then  
          ((t++))
          touch "res$t" 
      fi   
  echo "$BANDIT24_PASS $PIN" >> "res$t"
  done
  ############
  文心一言优化版本
  
  #!/bin/bash   
  BANDIT24_PASS="gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8"    
  t=1  
  file_index=1  
  for PIN in $(seq -w 0000 9999); do    
      if (( $(echo "$PIN % 500" | bc) == 0 )); then  
          file_index=$((file_index + 1))  
          t=$file_index  # 如果你还需要变量t来跟踪文件索引，可以这样做  
          touch "res$t"   
      fi    
      echo "$BANDIT24_PASS $PIN" >> "res$file_index"  
  done
  
  ####
  在 Bash 脚本中，bc 是一个任意精度的计算器语言，它支持浮点数运算、算术运算、逻辑运算等。在你给出的代码片段中，bc 被用来执行模数（余数）运算。
  
  具体来说，$PIN % 500 是一个尝试计算 $PIN 除以 500 的余数的表达式，但 Bash 的内建算术扩展不支持直接处理这种格式（特别是当 $PIN 是一个字符串形式的数字时）。因此，我们需要使用外部工具来执行这个操作。
  
  echo "$PIN % 500" | bc 这部分代码做了以下几件事：
  
  echo "$PIN % 500"：输出一个字符串，这个字符串是 $PIN 变量和一个 % 500 字符串的组合。
  |：管道操作符，它会把前一个命令的输出作为后一个命令的输入。
  bc：这是命令行计算器，它会读取从管道传递来的字符串，并尝试计算它。在这种情况下，bc 会解析 % 为模数运算符，并返回 $PIN 除以 500 的余数。
  然后，if (( ... == 0 )); then 这部分代码会检查 bc 计算出的余数是否等于 0。如果是，那么 then 后面的代码块就会被执行。
  
  简而言之，bc 在这里被用作一个外部工具，来执行 Bash 内建算术扩展无法直接处理的模数运算
  ```
  
- ```shell
  #!/bin/bash  
  for((i=1; i<=100; i++))
  do
      cat "res$i" | nc localhost 30002 >> ans
      sleep 2
  done
  
  #!/bin/bash  
  for((i=2; i<=22; i++))
  do
      print "res$i" | nc localhost 30002 >> ans
      sleep 2
  done
  
  
  #!/bin/bash  
  for((i=1; i<=30; i++))  
  do  
      file="res$i"  
      # 检查文件是否存在  
      if [ -f "$file" ]; then
      	echo "$file start"
          cat "$file" | nc localhost 30002 >> $file2 
          echo "$file end"
      else  
          echo "文件 $file 不存在"  
      fi  
  done
  
  
  #!/bin/bash  
  cat res2 | nc localhost 30002 >> ans
  sleep 2
  cat res3 | nc localhost 30002 >> ans
  sleep 2
  cat res4 | nc localhost 30002 >> ans
  sleep 2
  cat res5 | nc localhost 30002 >> ans
  sleep 2
  cat res6 | nc localhost 30002 >> ans
  sleep 2
  cat res7 | nc localhost 30002 >> ans
  sleep 2
  cat res8 | nc localhost 30002 >> ans
  sleep 2
  cat res9 | nc localhost 30002 >> ans
  sleep 2
  cat res10 | nc localhost 30002 >> ans
  sleep 2
  cat res11 | nc localhost 30002 >> ans
  sleep 2
  cat res12 | nc localhost 30002 >> ans
  sleep 2
  cat res13 | nc localhost 30002 >> ans
  sleep 2
  cat res14 | nc localhost 30002 >> ans
  sleep 2
  cat res15 | nc localhost 30002 >> ans
  sleep 2
  cat res16 | nc localhost 30002 >> ans
  sleep 2
  cat res17 | nc localhost 30002 >> ans
  sleep 2
  cat res18 | nc localhost 30002 >> ans
  sleep 2
  cat res19 | nc localhost 30002 >> ans
  sleep 2
  cat res20 | nc localhost 30002 >> ans
  sleep 2
  cat res21 | nc localhost 30002 >> ans
  sleep 2
  cat res22 | nc localhost 30002 >> ans
  done
  
  
  
  #!/bin/bash  
  cat res15 | nc localhost 30002 >> ans
  sleep 5
  cat res16 | nc localhost 30002 >> ans
  sleep 5
  cat res17 | nc localhost 30002 >> ans
  sleep 5
  cat res18 | nc localhost 30002 >> ans
  sleep 5
  cat res19 | nc localhost 30002 >> ans
  sleep 5
  cat res20 | nc localhost 30002 >> ans
  sleep 5
  cat res21 | nc localhost 30002 >> ans
  done
  ```
  
- ```python
  ## python2写法
  from pwn import *
  
  r = remote('localhost', 30002)
  for i in range(0, 10):
      for j in range(0, 10):
          for k in range(0, 10):
              for p in range(0, 10):
                  flag = str(i) + str(j) + str(k) + str(p)
                  s = "gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8 "+ flag
                  r.sendline(s)
                  response = r.recvline().decode() # 注意要解码
                  if 'Wrong!' not in response:
                      print 'Correct! ' + response
                
    # python3 写法
  from pwn import *
  
  r = remote('localhost', 30002)
  for i in range(0, 10):
      for j in range(0, 10):
          for k in range(0, 10):
              for p in range(0, 10):
                  flag = str(i) + str(j) + str(k) + str(p)
                  s = "gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8 "+ flag
                  r.sendline(s)
                  response = r.recvline().decode()
                  if 'Wrong!' not in response:
                      print ('Correct! ' + response)
                      
                      # 获得密码iCi86ttT4KSNe1armKiwbQNmB3YJP3q4
  ```
  
- 
  
- 获得所有结果存到ans文件中

- grep -A 2 "Correct!" ans

-     -A 查询之后 。-B查询之前

- 获得密码：iCi86ttT4KSNe1armKiwbQNmB3YJP3q4





## lv25-26

* 目标：
  
  * Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not /bin/bash, but something else. Find out what it is, how it works and how to break out of it.

* 命令学习：
  
  * ssh, cat, more, vi, ls, id, pwd
  
  * more
    
    * 分页显示文本文件的内容  
      原文链接：[more命令 &#8211; 分页显示文本文件内容 &#8211; Linux命令大全(手册)](https://www.linuxcool.com/more)
    * more 参数 文件名  
    * 
  
  * vim
    
    * ：ex 使用ex底层编辑模式  

* 解题步骤：
  
  * ssh -p 2220 bandit25@bandit.labs.overthewire.org
     iCi86ttT4KSNe1armKiwbQNmB3YJP3q4
  
  * ssh bandit26@localhost -i bandit26.sshkey -p 2220
  
  * 知识点：/etc/passwd目录
  
  * cat /etc/passwd | grep bandit26
    
    * bandit26:x:11026:11026:bandit level 26:/home/bandit26:/usr/bin/showtext
  
  * cat /usr/bin/showtext
    
    * #!/bin/sh
      
      export TERM=linux
      
      exec more ~/text.txt
      exit 0
    
    * **more**指令，该指令是一个文本过滤器在终端界面足够小到只能显示一行的时候起作用，
  
  * 拉小终端后执行：ssh bandit26@localhost -i bandit26.sshkey -p 2220
  
  * 按v 进入vim模式
  
  * esc后输入：进入vim命令模式，输入:e /etc/bandit_pass/bandit26
  
     * :e 编辑模式
  
  * 获得密码：s0773xxkk0MXfdqOfPRVr9L3jJBUOgCZ

## lv26-27

- 目标：
  
  - Good job getting a shell! Now hurry and grab the password for bandit27!

- 命令学习：
  
  - ls

- 解题步骤：
  
  - 借助lv25-26，进入到vim文档中
  
  - :set shell=/bin/sh
  
  - :shell
  
  - ls -la
  
  -  ./bandit27-do cat /etc/bandit_pass/bandit27
  
  - 获得密码：upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB

## lv27-28

* 目标：

  * There is a git repository at `ssh://bandit27-git@localhost/home/bandit27-git/repo` via the port `2220`. The password for the user `bandit27-git` is the same as for the user `bandit27`.

    Clone the repository and find the password for the next level.

* 命令学习：

  * git

* 解题步骤：

  * ssh -p 2220 bandit27@bandit.labs.overthewire.org 
    * upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB
  * mkdir /tmp/bandit27tmp
  * cd /tmp/bandit27tmp
  * git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
  * ls
  * cd repo/
  * ls
  *  cat README
  * 获得密码：Yz9IpL0sBcCeuG7m9uQFt8ZNpS4HZRcN

## lv28-29

* 目标：

  * There is a git repository at `ssh://bandit28-git@localhost/home/bandit28-git/repo` via the port `2220`. The password for the user `bandit28-git` is the same as for the user `bandit28`.

    Clone the repository and find the password for the next level.

* 命令学习：

  * git

* 解题步骤：

  * ssh -p 2220 bandit28@bandit.labs.overthewire.org

    * Yz9IpL0sBcCeuG7m9uQFt8ZNpS4HZRcN

  * mkdir /tmp/bandit28tmp

  * cd /tmp/bandit28tmp

  * git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo

  * git log

    * ```vim
      * commit 14f754b3ba6531a2b89df6ccae6446e8969a41f3 (HEAD -> master, origin/master, origin/HEAD)
        Author: Morla Porla <morla@overthewire.org>
        Date:   Thu Oct 5 06:19:41 2023 +0000
		  
      fix info leak
      
        commit f08b9cc63fa1a4602fb065257633c2dae6e5651b
        Author: Morla Porla <morla@overthewire.org>
        Date:   Thu Oct 5 06:19:41 2023 +0000
		  
      add missing data
      
        commit a645bcc508c63f081234911d2f631f87cf469258
        Author: Ben Dover <noone@overthewire.org>
        Date:   Thu Oct 5 06:19:41 2023 +0000
	    ```
    
  * git show 14f754b
  
  * 获得密码：4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7



## lv29-30

* 目标：

  * There is a git repository at `ssh://bandit29-git@localhost/home/bandit29-git/repo` via the port `2220`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

    Clone the repository and find the password for the next level.

* 命令学习：

  * git

* 解题步骤：

  * ssh -p 2220 bandit29@bandit.labs.overthewire.org

    *  4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7

  * mkdir /tmp/bandit29tmp

  * cd /tmp/bandit29tmp

  * git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo

  * ls

  * cd repo/

  * git branch -a

  * git checkout  remotes/origin/dev

  * git log

  * git show

    * ```
      Author: Morla Porla <morla@overthewire.org>
      Date:   Thu Oct 5 06:19:43 2023 +0000
      
          add data needed for development
      
      diff --git a/README.md b/README.md
      index 1af21d3..a4b1cf1 100644
      --- a/README.md
      +++ b/README.md
      @@ -4,5 +4,5 @@ Some notes for bandit30 of bandit.
       ## credentials
      
       - username: bandit30
      -- password: <no passwords in production!>
      +- password: qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL
      ```

    

  * 获得密码：qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL



## lv30-31

* 目标：

  * There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo` via the port `2220`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

    Clone the repository and find the password for the next level.****

* 命令学习：

  * git
    * git show-ref  显示本地存储库的所有可用的引用以及关联的提交ID

* 解题步骤：

  * ssh -p 2220 bandit30@bandit.labs.overthewire.org
    * qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL
  * mkdir /tmp/bandit30tmp
  * cd /tmp/bandit30tmp
  * git clone ssh://bandit30-git@localhost:2220/home/bandit30-git/repo
  * git show-ref  
    * 49ebc0513539a56d3626f3121ff4e72585064047 refs/heads/master
      49ebc0513539a56d3626f3121ff4e72585064047 refs/remotes/origin/HEAD
      49ebc0513539a56d3626f3121ff4e72585064047 refs/remotes/origin/master
      84368f3a7ee06ac993ed579e34b8bd144afad351 refs/tags/secret
  * git show 84368f
  * 获得密码：fb5S2xb7bRyFmAvQYQGEqsbhVyJqhnDy

# 模板

* 目标：

* 命令学习：

* 解题步骤：
  * ssh -p 2220 bandit @bandit.labs.overthewire.org
  * 获得密码：
