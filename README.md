# Nuke-Net
```
  ______        __                 ______        __   
 |   _  \.--.--|  |--.-----.______|   _  \.-----|  |_ 
 |.  |   |  |  |    <|  -__|______|.  |   |  -__|   _|
 |.  |   |_____|__|__|_____|      |.  |   |_____|____|
 |:  |   |                        |:  |   |           
 |::.|   |                        |::.|   |           
 `--- ---'                        `--- ---'           
Nuke-Net     Special-OP-Ajax-Spider   Scare_Sec_Hackers
-------------------------------------------------------  
```

Nuke-Net is a VERY VERY over powered and ridiculous web crawler that is well- very very noisy XD read more here


# why?
well simple, i was bored i am currently working on the project red-rabbit version 5 now ( see version 4 here https://ArkAngeL43/Red-Rabbit-V4)<br>
and quite frankly i just figured why not test the current knowlege i have with golang, so to resume that lets talk about what this tool does 

# brief DESC

```
for simplicity 

1 => Crawl URL's
2 => Download the HTML files
3 => Admin test your target
4 => Tests SQLI against the target
5 => grabs the response headers
6 => parses complex urls
7 => writes server domain IP's to a file 
8 => writes test output to a file 
9 => writes SQLI tests to a file
10 => port scans domains and your target 

for advanced


when this crawler or spider starts off it attempts to download your targets HTML file ( this is a customizable option ) will grab the request headers, parse the IP, parse the domain, parse the URL and strings, parse the requests, save the requests and write all of your data in a file 

when it is done testing over 100+ admin panel finding payloads ( this goes based off the requests ) then it will start scraping, first it will grab the URL's headers like this 

[  INFO  ]  Etag	 -> ["3147526947"]
	[  INFO  ]  Expires	 -> [Mon, 27 Dec 2021 05:31:04 GMT]
	[  INFO  ]  Server	 -> [ECS (mic/9A9C)]
	[  INFO  ]  Accept-Ranges	 -> [bytes]
	[  INFO  ]  Cache-Control	 -> [max-age=604800]
	[  INFO  ]  Content-Type	 -> [text/html; charset=UTF-8]
	[  INFO  ]  Date	 -> [Mon, 20 Dec 2021 05:31:04 GMT]
	[  INFO  ]  Age	 -> [441049]
	[  INFO  ]  Last-Modified	 -> [Thu, 17 Oct 2019 07:18:26 GMT]
	[  INFO  ]  Vary	 -> [Accept-Encoding]
	[  INFO  ]  X-Cache	 -> [HIT]
 	[  INFO  ]  -> SKIPPED HTML DOWNLOAD, FLAG NOT PARSED
46 (BYTES WRITTEN TO FILE)

then will retrieve the domain name as seen below

	[ INFO ]  FOUND DOMAIN NAME => example.com

will find the IP of the domain and port scan it 

	[*] Scan Results for   ├ example.com (0.0.0.0)
	[+]			┡ 443	https
	[+]			┡ 80	http


then grab the server, status, and the domain IP range

[ INFO ]  FOUND DOMAIN IP => [0000:00000:000:0:000:0000:0000:0000 0.0.0.0]75
	[ INFO ]  FOUND SERVER => ECS (mic/9ABC)
	[ INFO ]  RESPO STATUS => 200OK	[ INFO ]  FOUND URL => https://www.iana.org/domains/example 

then continues to test the SQLI against the URl

 	[  INFO  ] Server HAS PASSED ALL INJECTIONS, NOT VULNERABLE
 	[  INFO  ] Server HAS PASSED ALL INJECTIONS, NOT VULNERABLE
 	[  INFO  ] Server HAS PASSED ALL INJECTIONS, NOT VULNERABLE
 	[  INFO  ] Server HAS PASSED ALL INJECTIONS, NOT VULNERABLE
 	[  INFO  ] Server HAS PASSED ALL INJECTIONS, NOT VULNERABLE
 	[  INFO  ] Server HAS PASSED ALL INJECTIONS, NOT VULNERABLE
 	[  INFO  ] Server HAS PASSED ALL INJECTIONS, NOT VULNERABLE
 	[  INFO  ] Server HAS PASSED ALL INJECTIONS, NOT VULNERABLE
 	[  INFO  ] Server HAS PASSED ALL INJECTIONS, NOT VULNERABLE
 	[  INFO  ] Server HAS PASSED ALL INJECTIONS, NOT VULNERABLE
 	[  INFO  ] Server HAS PASSED ALL INJECTIONS, NOT VULNERABLE
 	[  INFO  ] Server HAS PASSED ALL INJECTIONS, NOT VULNERABLE
 	[  INFO  ] Server HAS PASSED ALL INJECTIONS, NOT VULNERABLE
 	[  INFO  ] Server HAS PASSED ALL INJECTIONS, NOT VULNERABLE
 	[  INFO  ] Server HAS PASSED ALL INJECTIONS, NOT VULNERABLE
 	[  INFO  ] Server HAS PASSED ALL INJECTIONS, NOT VULNERABLE
 	[  INFO  ] Server HAS PASSED ALL INJECTIONS, NOT VULNERABLE
 	[  INFO  ] Server HAS PASSED ALL INJECTIONS, NOT VULNERABLE
 	[  INFO  ] Server HAS PASSED ALL INJECTIONS, NOT VULNERABLE



for every URL it finds it will crawl that URL and still continue the search for the other URL's and continue to crawl until it runs out or you come across

eaither this error -> Get "https://www.scanme.org/admin/": dial tcp [2600:3c01::f03c:91ff:fe18:bb2f]:443: connect: connection refused
<br>
or this one -> panic: runtime error: invalid memory address or nil pointer dereference
[signal SIGSEGV: segmentation violation code=0x1 addr=0x40 pc=0x2293]
<br>
this is not due to the script this is due to its end point, when the script hits a dead end or a domain doesnt work correctly it will log or panic the error, some domains you can even get the GET error or POST error to the URl, this is probobly due to the DIAL error with the URL not accepting connections during the current time 

<br>


```
<br>
<br>
# usages 

```
basic usage 
                |=> HTTPS URL                 |=> Domain Name         |=> Base URL or HTTP URL     |=> for every URL downl;oad every HTML index
                |                             |                       |                            |
go run main.go -target https://www.scanme.org -domain www.example.org -base http://www.example.com -filedfel

NOTE => -filedfel IS OPTIONAL AND IS NOT NEEDED ( it is suggested cause well-- you are like downloading 800+ HTML files ( cries why ) 

```

# where is the output stored 
<br>
ALL OUTPUT IS STORED IN THE `OUTPUT` FOLDER
<br>
<br>
```
|FILE LOCATION |  NAME               | WHAT'S SAVED |
|--------------|---------------------|--------------|
|output        | ip-out.txt          | IP OF DOMAIN |
|output        | out.txt             | URLS FOUND   |
|output        | tests_pass_list.txt | TEST RESULTS |
```
![demo](demo.png)


