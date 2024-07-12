# natas

每一关的地址是http://natasX.natas.labs.overthewire.org，其中X代表当前关数，默认用户名是nataX（eg.natas0 是level0的用户名），通过当前的一关获取进入下一关的密码。所有密码存储在/etc/natas_webpass/中（eg.level5的密码存储在/etc/natas_webpass/natas5，只能在第四关和第五关能够读取密码）

原文链接：https://blog.csdn.net/tempulcc/article/details/108758417

## level0

```
Username: natas0
Password: natas0
URL:      http://natas0.natas.labs.overthewire.org
```

* 谷歌浏览器打开开发者选项
* 获得密码：0nzCigAq7t2iALyvU9xcHlYN4MlkIwlq
* <!--The password for natas1 is 0nzCigAq7t2iALyvU9xcHlYN4MlkIwlq -->



## Natas Level 0 → Level 1

```
Username: natas1
URL:      http://natas1.natas.labs.overthewire.org
```

* <!--The password for natas2 is TguMNxKo1DSa1tujBLuZJnDUlCcUAPlI -->
* TguMNxKo1DSa1tujBLuZJnDUlCcUAPlI

## Natas Level 1 → Level 2

```
Username: natas2
URL:      http://natas2.natas.labs.overthewire.org
```

*  发现 http://natas2.natas.labs.overthewire.org/files/pixel.png

* 访问files目录

* 发现 users.txt

* 获得：

* ```
  # username:password
  alice:BYNdCesZqW
  bob:jw2ueICLvT
  charlie:G5vCxkVV3m
  natas3:3gqisGdR0pjm6tpkDKdIWO2hSvchLeYH
  eve:zo4mJWyNj2
  mallory:9urtcpzBmH
  ```

## Natas Level 2 → Level 3

```
Username: natas3
URL:      http://natas3.natas.labs.overthewire.org
```

* 开发模式查看提示：<!-- No more information leaks!! Not even Google will find it this time... -->

* 谷歌通过爬robots.txt决定是否爬取文件

* 访问   http://natas3.natas.labs.overthewire.org/robots.txt

* 获得：

* ```
  User-agent: *
  Disallow: /s3cr3t/
  ```

* 访问  http://natas3.natas.labs.overthewire.org/s3cr3t/

* 找到user.txt
* 获得密码：natas4:QryZXc2e0zahULdHrtHxzyYkj59kUxLQ

## Natas Level 3 → Level 4

```
Username: natas4
URL:      http://natas4.natas.labs.overthewire.org
```

* curl -isu natas4:QryZXc2e0zahULdHrtHxzyYkj59kUxLQ natas4.natas.labs.overthewire.org --referer "http://natas5.natas.labs.overthewire.org/"
* The password for natas5 is 0n35PkggAPm2zbEpOU802c0x0Msn1ToK
* 或者
* 用brup suite抓包后
* proxy 抓包修改referer为 http://natas5.natas.labs.overthewire.org/
  * 保证intercept 为 intercept  is on
  * 修改referer后点击forward
  * 返回原来页面即可查看natas5答案

## Natas Level 4 → Level 5

```
Username: natas5
URL:      http://natas5.natas.labs.overthewire.org
```