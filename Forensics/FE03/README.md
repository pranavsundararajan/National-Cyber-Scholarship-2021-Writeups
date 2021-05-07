# FE03 (100 pts)

## Description
Download the file and find a way to get the flag from the docker image.

## Approach
Technically, we should open this using docker and go through the files, but I decided to do some digging around since there were only a handful of directories with one layer in each as shown below (and I didn't want to download docker for 300 mb)
[](FE03Terminal.jpg)
Working our way from the bottom up, we find this in the 2nd to last directory, which we can assume is the flag since it says flag.txt

## Flag
`SiMpLeFilESysTemForens1Cs`
