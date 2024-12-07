# Easy 32 - 10 Point
> 10+22
>
> INKEMUSTKR5UKYLTPFPWM33SL4ZTEX3QMVXXA3DFPU======
### Solution
From the name of the challenge itself and the description that were given, it safe to assume that this is basically Base32 encryption.

**From [Wikipedia](https://en.wikipedia.org/wiki/Base32#:~:text=Base32%20is%20an%20encoding%20method,5%20bits%20(25).)**
```
Base32 is an encoding method based on the base-32 numeral system.
It uses an alphabet of 32 digits, each of which represents a
different combination of 5 bits (25).
```
It's basically almost the same as Base64, this one is just a toned down version of it. We can decode the given Base32 text using CyberChef or Linux terminal.
```
┌──(ibnuraffi㉿kali)-[~]
└─$ echo "INKEMUSTKR5UKYLTPFPWM33SL4ZTEX3QMVXXA3DFPU======" | base32 -d
CTFRST{Easy_for_32_people}
```
