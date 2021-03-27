# A writeup on new account from cybertalents, Marathon CTF.

- Challenge Name: `new account`
- Level: `Easy`
- Points: `50`
- Category: `Digital Forensics`

## Challenge Description
>> an attacker after compromising the machine added a new account as admin.
>> 
>> can you find the name of the new account? 
>> 
>> flag format : flag{md5 of string}


## Solution
I'm not gonna lie but this took a longer time than it should,
but i looked straight for the `logon logs` and found out a log that has the username:`Sam`
so i took it and turned it to an md5 string.

- https://www.md5hashgenerator.com/
- **`Your Hash: ba0e0cde1bf72c28d435c89a66afc61a`**
- **`Your String: Sam`**

Flag: `flag{ba0e0cde1bf72c28d435c89a66afc61a}`
