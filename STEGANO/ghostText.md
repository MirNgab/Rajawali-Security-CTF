# ghostText - 10 Points
> ?HAy?HAy mimin menyembunyikan sesuatu di gambar ini Bisakah kamu menemukannya

_**File :**_ https://ctf.rajawalisecteam.eu.org/assets/uploads/hide.png
### Solution
![hide](https://github.com/user-attachments/assets/cad8248f-61b3-4af2-9c66-336da332434c)

Trying bunch of commands like exiftool and binwalk didn't go smoothly whatsoever, even analyzing the picture's hex using xxd didn't give me anything, it's probably has to do with LSB or MSB encoding at this point, so i used zsteg.
```
┌──(ibnuraffi㉿kali)-[~/Desktop/rajawalictf]
└─$ zsteg hide.png 
b1,g,msb,xy         .. file: OpenPGP Secret Key
b1,rgb,lsb,xy       .. text: "CTFRST{h1d3_t3xt_1n_im4g3}"
b2,r,msb,xy         .. text: "_UUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUU"
b2,g,msb,xy         .. text: "WUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUU"
b2,b,msb,xy         .. text: ["U" repeated 239 times]
b2,rgb,msb,xy       .. text: ["U" repeated 204 times]
b2,bgr,msb,xy       .. text: "}]UUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUU"
b2,abgr,msb,xy      .. text: ["W" repeated 186 times]
b4,r,msb,xy         .. text: ["w" repeated 221 times]
b4,g,msb,xy         .. file: RDI Acoustic Doppler Current Profiler (ADCP)
b4,b,msb,xy         .. text: ["w" repeated 222 times]
b4,rgb,msb,xy       .. text: ["w" repeated 152 times]
b4,bgr,msb,xy       .. text: ["w" repeated 151 times]
b4,abgr,msb,xy      .. file: RDI Acoustic Doppler Current Profiler (ADCP)
```
Sometimes you gotta appreciate tools like this is free and you can use it everytime whenever you want
