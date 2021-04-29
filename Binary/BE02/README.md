# BE02 (100 pts)

## Description
Download the file and find a way to get the flag

[rot13](rot13)

## Approach
Doing some initial fuzzing, we find that when we put in any arbitrary long input, the buffer overflows and the flag is output. 
```./rot13
===================================
ROT IN sHELL :: ROT13's your input!
===================================
> zzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzz

Segmentation fault.
*** stack smashing detected ***: <unknown> terminated
Aborted (core dumped)

Flag: luckyNumber13
```

## Flag
```
luckyNumber13
```
