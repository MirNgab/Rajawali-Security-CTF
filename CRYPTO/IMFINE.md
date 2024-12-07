# IMFINE - 10 Points
> Ini masi Berhubungan dengan Chall ABSTRACT. HGQADG{4qq1o3_h1uw3a} coba pecahkan

_**Hint :**_ f(x)=3x+1 Default
### Solution
This isn't atbash this time so i start this by just searching the name of this challenge and add cipher in the end, hoping that google will autocorrect my search result, and it did. I got what it's called Affine Cipher.

**From [Wikipedia](https://en.wikipedia.org/wiki/Affine_cipher#)**
```
The affine cipher is a type of monoalphabetic substitution cipher,
where each letter in an alphabet is mapped to its numeric equivalent,
encrypted using a simple mathematical function, and converted back
to a letter.
```
I'm not really the type of person who can understand math in one swing, but the whole encryption formula is kind simple

**f(x)=(ax+b) mod m**

Though i'm still lazy to understand it, with the help of the hint you can make this a lot more simple, by just drag the encrypted flag into CyberChef

![image](https://github.com/user-attachments/assets/abff9c04-2ec7-441b-99c6-db0632791dc4)

The a and b can be replaced with the given value on the hint, and after that just let CyberChef cook, and there you have it

**CTFRST{4ff1n3_c1ph3r}**
## Unintended Way
You can kind of do this in an unintended way if you get what the challenge is all about and how the encrypted flag is formed. Since this challenge is said to be an affine cipher, you can get the idea on what the actual flag is.
```
4qq1o3
```
4 in flag usually means A, 1 usually means I and 3 usually means E. You can see that affine uses 2 f's which from the looks of the encrypted flag, it kind of like it's trying to say 4ff1n3, I hope you started getting the idea here. 
```
h1uw3a
```
And for this one, from the position of 1 and 3, it kind of looks like it's trying to say c1ph3r, in which yeah it is. And for the format of the flag, it's safe to assume that it's just the same as ever, CTFRST{}.

This is the reason why i think the content of the flag in CTF is should be random gibberish instead of formal one like this, if the circumstances are at the correct way, you can kind of cheese your way out to solve it.
