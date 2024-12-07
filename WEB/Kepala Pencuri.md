# Kepala Pencuri - 10 Points
> Bantu aku mencari kepala pencuri

_**Link :**_ https://ctf.rajawalisecteam.eu.org/assets/uploads/headku.php

_**Hint :**_ Kepala pencuri harus di tembak
### Solution
Kepala in english means head, so i assume i only need to just see the head request in order to get the flag, so i use curl with **-I** parameter before the link in which, it give me the flag.

You can do this using BurpSuite but, i prefer simple way like this
```
┌──(ibnuraffi㉿kali)-[~/Desktop/rajawalictf]
└─$ curl -I https://ctf.rajawalisecteam.eu.org/assets/uploads/headku.php
HTTP/2 200 
flag: CTFRST{_Random_String_HEAD}
message: zuhahahaxD-You-Never-Find-Anything-In-Here!
message2: Please-Go-Deeper!
content-type: text/html; charset=UTF-8
date: Sat, 07 Dec 2024 11:48:44 GMT
alt-svc: h3=":443"; ma=2592000, h3-29=":443"; ma=2592000, h3-Q050=":443"; ma=2592000, h3-Q046=":443"; ma=2592000, h3-Q043=":443"; ma=2592000, quic=":443"; ma=2592000; v="43,46"
```
