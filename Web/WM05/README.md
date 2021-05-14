# WM05 (250 pts)

## Description
Access the site at https://cfta-wm05.allyourbases.co, then find and read the contents of the flag file, to get the flag.

## Approach
Initially, I decided to just look through some of the directories and see what was going on; I quickly found out however that there are much too many directories to simply look through. After going to the page source, we notice this value for the display as none.
```
<div class="container h-mt-5">
            <h1>Learn Linux</h1>
            <h2>Look around a typical Linux system interactively to understand the structure</h2>
            <div class="c-well">
                <form style="display: none">
                    <input type="text" id="path" class="c-form-input" name="path" value="/"><br>
                    <input type="submit" id="submit" class="c-btn c-btn--primary c-btn--block" value="Submit" type="button">
```
When we change this to true, we get access to a shell input, albeit critically restricted. 
