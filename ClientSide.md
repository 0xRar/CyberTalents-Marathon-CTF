# A writeup on Client Side from cybertalents, Marathon CTF.
- Challenge Name: `Client Side`
- Level: `Easy`
- Points: `50`
- Category: `Web Security`

## Challenge Description
>> Client side password check isn't secure, is it ? 
>> 
>> The password is your flag. Note: Flag format flag{XXXXXXXXXX}

## First Look
First of all this is cursed, and really bad code lol
![image](https://user-images.githubusercontent.com/33517160/112241044-8fa78d80-8c5a-11eb-9f01-2a0875a26cd0.png)


## Solution
All you have to do is to take the value of the `checkpass.substring`
take the values from `(0,split)` up to `(split*8, split*9)` and you got you're flag,

or you can make a simple script like this:

Script By [codaholikid](https://twitter.com/codaholikid)
```
#!/usr/bin/env python3
# @author: codaholikid

password = [0]*9

password[0] = 'd!}'
password[1] = '4dd'
password[2] = '$_b'
password[3] = '3_i'
password[4] = '$id'
password[5] = 'nt_'
password[6] = 'li3'
password[7] = 'g{C'
password[8] = 'fla'

print("".join(password[::-1]))
```

Flag: `flag{Cli3nt_$id3_i$_b4ddd!}`
