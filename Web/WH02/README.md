# WH02 (500 pts)

## Description
Access the site at https://cfta-wh02.allyourbases.co and find a way to get the flag

## Approach
Upon visiting the site, nothing stands out, so we can do some fuzzing which includes some sort of dirbusting; I used dirb for this as shown below.

![](dirb.jpg)

We see a git directory underneath, so we can assume there is an open git index that we can access. There are multiple ways to dump this, but I decided to use this [script](https://github.com/internetwache/GitTools) which worked perfectly with the command below.
