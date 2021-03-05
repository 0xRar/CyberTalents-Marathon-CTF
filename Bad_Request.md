# A writeup on Bad Request from cybertalents, Marathon CTF.

- Challenge Name: `Bad Request`
- Level: `Medium`
- Points: `100`
- Category: `Web Security`

## Challenge Descreption
>> we are working on an api for our website , 
>> we didn't decide if YAML would be accurate or not but it is still under construction , we hope our passwd file is secure.


## First Look
as we see we got a json document `api_data	"The api is still under construction, updates coming soon!`
and taking a look at the cookies with the cookie editor we have a cookie called `data`:`YXBpX2RhdGE6IFRoZSBhcGkgaXMgc3RpbGwgdW5kZXIgY29uc3RydWN0aW9uLCB1cGRhdGVzIGNvbWluZyBzb29uIQ==`
when we decode the base64 we get:`api_data: The api is still under construction, updates coming soon!`,
basiclly nothing, but when you think about it it makes sense ofcourse it has something to do with YAML
so look up `YAMl Deserialization` its a YAML RCE.

I found an intereseting payload `yaml: !!python/object/apply:subprocess.check_output ['id']` and it worked
but 
