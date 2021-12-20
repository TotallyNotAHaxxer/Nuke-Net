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




```
