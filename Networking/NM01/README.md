# NM01 (250 pts)

## Description
Retrieve output from network endpoint at cfta-nm01.allyourbases.co port 8017 and figure out how to get the flag.

## Approach
When we connect to the network, we receive a hex string, as shown below.
```
pranav$ nc cfta-nm01.allyourbases.co 8017
\x4F\x56\x46\x49\x50\x48
```
We also notice that the hex changes everytime, much too fast to decode it by hand to ASCII and type it in. Initially, I tried to write a python script using sockets to do this, but had issues with the formatting and no matter what I tried it didn't work. However, I noticed that the network cycled through a determined set of hex strings, so after a certain amount of relatively short time the same hex may show up. Thus, I picked one, decoded it, and simply spammed it as below.
```
pranav$ echo "OVFIPH" | nc cfta-nm01.allyourbases.co 8017
\x45\x47\x55\x47\x49\x43
Correct! - Flag: o[hex]=>i[ascii]=:)
```
To get to this point, it only took 6 tries. Of course this isn't the intended solution, but hey, a flag is a flag.

## Flag
`o[hex]=>i[ascii]=:)`
