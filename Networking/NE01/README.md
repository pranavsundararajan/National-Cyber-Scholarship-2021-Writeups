# NE01 (100 pts)

## Description
There is a TCP network service running on cfta-ne01.allyourbases.co. Find it to get the flag after you connect. Note: The target has many open ports - only one is the correct one. The correct port will identify itself with ID: ne01 after you connect.

## Approach
Since we're scanning for ports, we can use nmap to find the TCP one. 
```
pranav@pranav-VirtualBox:~$ nmap -Pn cfta-ne01.allyourbases.co
Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times will be slower.
Starting Nmap 7.91 ( https://nmap.org ) at 2021-04-29 18:10 EDT
Nmap scan report for cfta-ne01.allyourbases.co (34.251.231.207)
Host is up (0.11s latency).
Other addresses for cfta-ne01.allyourbases.co (not scanned): 52.210.101.44
rDNS record for 34.251.231.207: ec2-34-251-231-207.eu-west-1.compute.amazonaws.com
Not shown: 999 filtered ports
PORT     STATE SERVICE
1061/tcp open  kiosk
```
Now, we can netcat to the same address with the TCP port.
```
pranav@pranav-VirtualBox:~$ nc cfta-ne01.allyourbases.co 1061
ID: ne01
Flag: Nmap_0f_the_W0rld!
```
## Flag
Nmap_0f_the_W0rld!
