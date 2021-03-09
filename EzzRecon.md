# A writeup on EzzRecon from cybertalents, Marathon CTF.

- Challenge Name: `EzzRecon`
- Level: `Easy`
- Points: `50`
- Category: `Web Security`

## Challenge Descreption
>> Before thinking about the bugs , you should think where to find it.


## First Look
Looking at the challenge source code, there is a link which directs 
us to a random hosting service provider its probably a dns attack called dns poisoning
, but this challenge is just a recon challenge.

## Solution
As we can see in the source code we have this weird link that directs us to a random websites,
![image](https://user-images.githubusercontent.com/33517160/110498720-9f768c00-8108-11eb-8075-1adc1e7b9b45.png)

even though there is multiple ways to solve this i just went to the easier one which is a dns recon with `https://www.w3dt.net/tools/dnsrecon`

![image](https://user-images.githubusercontent.com/33517160/110499339-2e83a400-8109-11eb-92f5-1c794e6a58c9.png)
![image](https://user-images.githubusercontent.com/33517160/110499444-49561880-8109-11eb-894c-e6161ac9d9e6.png)



Flag: `flag_ezz_recon_all_the_time_congrats`
