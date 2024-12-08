# Tutor Hack Wa - 10 Points
> Hay mimin balik lagi, mimin punya document yang berisi tutor ngehack lohhh hihuhihihuhi

_**File :**_ https://www.mediafire.com/file/zg00zax48w4chwn/tutor_hack_wa.docx/file
### Solution
![image](https://github.com/user-attachments/assets/1448170f-adb2-40ce-8ff8-178a7baeaf53)

This scared me a little when i opened the doc for the first time, but let's get to the point. I first used exiftool just in case if some information can be gathered in which there's a message
```
┌──(ibnuraffi㉿kali)-[~/Desktop/rajawalictf]
└─$ exiftool tutor_hack_wa.docx 
ExifTool Version Number         : 13.00
File Name                       : tutor_hack_wa.docx
Directory                       : .
File Size                       : 54 kB
File Modification Date/Time     : 2024:12:08 18:55:43+07:00
File Access Date/Time           : 2024:12:08 18:55:57+07:00
File Inode Change Date/Time     : 2024:12:08 18:55:55+07:00
File Permissions                : -rw-rw-r--
File Type                       : DOCX
File Type Extension             : docx
MIME Type                       : application/vnd.openxmlformats-officedocument.wordprocessingml.document
Zip Required Version            : 20
Zip Bit Flag                    : 0x0808
Zip Compression                 : Deflated
Zip Modify Date                 : 2021:06:03 00:46:46
Zip CRC                         : 0x8fa87381
Zip Compressed Size             : 337
Zip Uncompressed Size           : 1133
Zip File Name                   : word/numbering.xml
Core Properties Xmlns           : http://schemas.openxmlformats.org/package/2006/metadata/core-properties
Core Properties Created Type    : dcterms:W3CDTF
Core Properties Created         : 2017-03-20T06:59:00Z
Core Properties Creator         : Penulis
Core Properties Last Modified By: FIND WITH COLOR <<<< This is the message
Core Properties Modified Type   : dcterms:W3CDTF
Core Properties Modified        : 2021-06-02T16:46:47Z
Core Properties Revision        : 3
Template                        : Normal.dotm
Total Edit Time                 : 4 minutes
Words                           : 7
Pages                           : 1
Characters                      : 62
Application                     : WPS Office
Doc Security                    : None
Paragraphs                      : 2
Scale Crop                      : No
Links Up To Date                : No
Characters With Spaces          : 68
Shared Doc                      : No
Hyperlinks Changed              : No
App Version                     : 16.000
```
I assume we need to find this flag using "color" which i don't know what it means by that until i realised when i opened the doc earlier, there's text with red color, so i tossed this doc file into CyberChef 
