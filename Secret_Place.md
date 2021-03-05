# A writeup on Secret Place from cybertalents, Marathon CTF.

- Challenge Name: `Secret Place`
- Level: `Easy`
- Points: `50`
- Category: `Malware Reverse Engineering`

## Challenge Descreption
>> There is a secret place in every executable.

## First Look
This one was pretty simple, Everytime i see a reverse engineering challenge i use Strings.

## Solution
`strings SecretPlace.exe`

I found a base64 encoded text `ZmxhZ3sweEFMV0FZU19DSEVDS19ZT1VSX0VNQkVEREVEX1JFU09VUkNFU30=`
So i decoded it `flag{0xALWAYS_CHECK_YOUR_EMBEDDED_RESOURCES}`

## Flag
`flag{0xALWAYS_CHECK_YOUR_EMBEDDED_RESOURCES}`
