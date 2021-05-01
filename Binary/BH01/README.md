# BH01 (500 pts)

## Description
Download the file and find a way to get the flag.

## Approach
When we run the [program](bh01.zip), we are asked for an input. After some initial fuzzing, we see that depending on the input we get varying lengths of the flag.  After a few minutes of more fuzzing, I got to this point.
```
~$ ./program
What is the magic word?
aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
Flag: ad#����*���E
Did you understand that?
~$ ./program
What is the magic word?
zzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzz
Flag: aLittLeObfuScatIonalCharAc9��
Did you understand that?
~$ ./program
What is the magic word?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Flag: aLittLeObfuScatIonalCharActEr
Did you understand that?
```


I noticed that with the letter "a", the flag was completely unrecognizable, while with "z", we pretty much have the whole flag and could do a little bit of brute force for only 3 characters. However, from this trend we can assume that the higher the ASCII value, the more of the flag we get, so I used the highest ASCII character "~" and got the flag. Although definitely not the *correct* solution, this did the trick and was definitely faster, and of course a flag is a flag.

## Flag
`aLittLeObfuScatIonalCharActEr`
