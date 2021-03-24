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
take the values from `(0,split)` up to `(split*8, split*9)` and you got you're flag.

Flag: `flag{Cli3nt_$id3_i$_b4ddd!}`
