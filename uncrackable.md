# A writeup on uncrackable from cybertalents, Marathon CTF.

- Challenge Name: `uncrackable`
- Level: `Medium`
- Points: `100`
- Category: `Digital Forensics`


## Challenge Description
>> john , can you crack this one ??



## First Look
They gave us the file as a gzip lets unzip it first,

- **`gzip -d uncrackable.tar.gz`**

after unziping it we still have the tar,

- **`tar -xf uncrackable.tar`**

after extracting the tar we get a pdf file called: `sec2.pdf`, when we try to open it
we can't because its encrypted with a pass.


## Solution
the challenge description is very useful for the solution,

we will use the `/usr/share/john/pdf2john.pl` john tool to get the pdf hash,

`perl /usr/share/john/pdf2john.pl sec2.pdf`, after doing that we get the pdf hash

- hash:``$pdf$2*3*128*-3904*1*16*9db3c812d6a0c898af95886f6d043eaa*32*44041e94111587f666acac56c794a44f00000000000000000000000000000000*32*1df5734e447cc82abf998e9befa24a81ca624be57d6759bb964b7c41ebc6a03a``

i saved my hash in a file called `sec2.hash`, lets crack the hash using brute force

`john --wordlist= /usr/share/wordlists/rockyou.txt`

i found a match but i tried to unlock the pdf i couldn't, i didint finish this one.
