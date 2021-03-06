# A writeup on password hint from cybertalents, Marathon CTF.

- Challenge Name: `password hint`
- Level: `Medium`
- Points: `100`
- Category: `Digital Forensics`

## Challenge Descreption
>> This a sam registry hive, can you find the password hint for a user called flag.

## Solution
A Registry Viewer `https://accessdata.com/product-download/registry-viewer-2-0-0`

![image](https://user-images.githubusercontent.com/33517160/110206820-1b669f00-7e91-11eb-816a-b2297bbaaf10.png)

We just need to decode the base64.
https://www.base64decode.org/

Flag: `flag{Great ! _parsing_Sam_Hive}`
