# A writeup on R3QUEST from cybertalents, Marathon CTF

- Challenge Name: `R3QUEST`
- Level: `Easy`
- Points: `50`
- Category: `Digital Forensics`

## Challenge Description
>> This request suspected as malicious in our SIEM, Can you find the attacker trace.
>> Flag format is flag{X.X.X.X}

```
HTTP/1.1 200 OK
Date: Mon, 27 Jul 2009 12:28:53 GMT
Server: Apache/2.2.14 (Win32)
Last-Modified: Wed, 22 Jul 2009 19:15:56 GMT
Accept-Ranges: bytes
ETag: "6238615a28:0"
Content-Length: 20
Content-Type: text/html

MDgzLzA3OS8zMzAvMDc0
```

## First Look
The only thing we can run with in this request is this base64 encoded string.

## Solution
As we can see its a base64 but when we decode it we get this XOR hex `083/079/330/074`,
lets decode it with CyberChef and get our flag,

CyberChef: `https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true)XOR(%7B'option':'Hex','string':'1'%7D,'Standard',false)`

![image](https://user-images.githubusercontent.com/33517160/112261387-d4442080-8c7c-11eb-968b-890efdb1294c.png)

from reading the challenge description we know that the flag is an ip address.

Flag: `flag{192.168.221.165}`
