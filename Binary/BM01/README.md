# BM01 (250 pts)

## Description
Download the file and find a way to get the flag.

## Approach
When we run the [program](bm01.zip), we get a prompt in Russian asking for the password. After some initial fuzzing, I decided to dig in using Ghidra. In the `main` function, I noticed that there is a strcmp as shown below which compares the input to a certain string at the address `DAT_001009c8`. 
