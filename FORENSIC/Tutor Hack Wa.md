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
It has to do with colors but i just can't find any idea on how to use this information, but there's one thing that i almost not pay my attention to, there's a second page and it's blank.

![image](https://github.com/user-attachments/assets/80bd1e7b-86ef-4b80-98ec-186abde91393)

So my idea was to use Ctrl + A and see if there's an invisible words that are highlighted in which, there are.

![image](https://github.com/user-attachments/assets/67358f8b-dbf7-4344-a881-13c09419ea16)

All you need to do now is just copy it and paste it to notepad or anything that would remove any style from a text, and you got the flag.

![image](https://github.com/user-attachments/assets/3ce8db90-f4ed-4f82-a9e3-22d17c81dfc3)

I think the intended way was try to extract the text by brute forcing every single color maybe? But again, simple challenge like this has many ways to solve it, not just one. Like you can get the flag by using this script
```py
from docx import Document

doc = Document('tutor_hack_wa.docx')

for paragraph in doc.paragraphs:
    for run in paragraph.runs:
        if run.font.color and run.font.color.rgb == (255, 255, 255):
            print(run.text)
```
```
┌──(myenv)(root㉿kali)-[/home/ibnuraffi/Desktop/rajawalictf]
└─# python extract_doc.py 
CTFRST{h1d3_t3xt_w1th_c0l0r}
```
