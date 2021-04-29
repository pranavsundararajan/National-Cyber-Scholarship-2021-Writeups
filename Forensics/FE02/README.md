# FE02 (100 pts)

## Description
> We're sure there's a flag at cfta-fe02.allyourbases.co - can you find it?

## Approach
Upon visiting the site, we see "Nothing to see here - try elsewhere?". During the competition, I only got a DNS error when visiting the link. Thus, I used the dig command on terminal which gathers info on DNS. Using `dig cfta-fe02.allyourbases.co txt` which shows the text record, we get this.
```
dig cfta-fe02.allyourbases.co txt

; <<>> DiG 9.10.6 <<>> cfta-fe02.allyourbases.co txt
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 53809
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 512
;; QUESTION SECTION:
;cfta-fe02.allyourbases.co.	IN	TXT

;; ANSWER SECTION:
cfta-fe02.allyourbases.co. 300	IN	TXT	"flag=unlimited_free_texts"

;; Query time: 32 msec
;; SERVER: 192.168.1.1#53(192.168.1.1)
;; WHEN: Thu Apr 29 17:18:56 EDT 2021
;; MSG SIZE  rcvd: 92
```
## Flag
`unlimited_free_texts`
