# FM01 (250 pts)

## Description
Download the file and find a way to get the flag.

## Approach
We're given an [image file](fm01.zip) so the first thing I do is preliminary checks (strings, exiftool, binwalk), and using `exiftool fm01.jpg` we can get the flag (exiftool output is abridged below since it has lot of extra info). As others have stated, this is assumedly a mistake with the challenge but a flag is a flag.
```
Desktop pranav$ exiftool fm01.jpg
ExifTool Version Number         : 12.21
File Name                       : fm01.jpg
Directory                       : .
File Size                       : 3.1 MiB
File Modification Date/Time     : 2021:03:12 09:03:30-05:00
File Access Date/Time           : 2021:04:24 22:09:23-04:00
File Inode Change Date/Time     : 2021:04:24 22:09:19-04:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Pixel Aspect Ratio              : 1
Photoshop Thumbnail             : (Binary data 10277 bytes, use -b option to extract)
Has Real Merged Data            : Yes
Writer Name                     : Adobe Photoshop
Reader Name                     : Adobe Photoshop 2021
Format                          : image/jpeg
Color Mode                      : RGB
ICC Profile Name                : 
Create Date                     : 2021:03:12 11:34:40Z
Modify Date                     : 2021:03:12 13:28:07Z
Metadata Date                   : 2021:03:12 13:28:07Z
History Action                  : saved, saved
History Instance ID             : xmp.iid:57de9171-9b29-714c-b64f-0791ca77a2bf, xmp.iid:434d9271-6b85-624d-8de6-7dc17c1a43a4
History When                    : 2021:03:12 13:28:07Z, 2021:03:12 13:28:07Z
History Software Agent          : Adobe Photoshop 22.2 (Windows), Adobe Photoshop 22.2 (Windows)
History Changed                 : /, /
Text Layer Name                 : flag: tr4il3r_p4rk
Text Layer Text                 : flag: tr4il3r_p4rk
Document Ancestors              : E25BCF5D355B2F2CE5EB55EC6B67C7AF
```
## Flag
`tr4il3r_p4rk`
