# A writeup on USB SN from cybertalents, Marathon CTF.

Challenge Name: `USB SN`
Level: `Medium`
Points: `100`
Category: `Digital Forensics`

## Challenge Description
>> The investigator needs to find the serial number of SANDISK USB 
>> flash drive which was connected to the machine he investigates.

## First Look
We see that the file provided is a `.evtx` which means ofc its an event log file,
the descreption was kinda tricky, first i searched for the key word USB i found couple
of them but as i remmember they said the flag is in md5 that tricked me i noticed somestuff
like, ![image](https://user-images.githubusercontent.com/33517160/110237377-ca1be580-7f4c-11eb-948c-c5e7c60f8b5a.png) 
&
![image](https://user-images.githubusercontent.com/33517160/110237435-254dd800-7f4d-11eb-8f13-ebf44c1702e0.png) 

when you put them as 1 text the length is 32 tried that but didin't work, thats when i tried to read the descreption again
they said **serial number**.

## Solution
Find/Search for the keyword `SANDISK` you will find the usb stick 
and the serial number at the end 
 - **WPDBUSENUMROOT\UMB\2&37C186B&0&STORAGE#VOLUME#_??_USBSTOR#DISK&VEN_SANDISK&PROD_ULTRA_USB_3.0&REV_1.00#`4C530000080406123243`&0#**
 - Serial Number: **`4C530000080406123243`**
 
 they want the output in md5 so use `https://www.md5hashgenerator.com/` to generate the hash.
 
 Flag:`a46a2bae610f55525c5995a5b831c768`
 
 Credits to "ItsFadinG".
