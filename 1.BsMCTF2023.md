# BxMCTF2023Writeup
First thing first thank you for the opportunity to participate in the CTF. Therefore, Im gonna share a few writeup for the challenges for the BxMCTF2023


**Category : General** 

1. Welcome to BxMCTF

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/3ba6b39a-5e81-4362-9f1b-4777806be6ab)

The Flag is already provided : ctf{check_out_our_sponsors!}

2. New Website 

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/14d93541-ddac-4c7b-b991-217a89f18701)

* The error message "DNS_PROBE_FINISHED_NXDOMAIN" typically appears in web browsers when there is a DNS (Domain Name System) resolution failure. It indicates that the DNS server was unable to resolve the domain name you entered into the browser's address bar.
* So maybe, there is previous record for the url. 
* Let use online dns checker tools : https://dnschecker.org/
* Insert your domain (url). 
* It will return a few of result.
* Scroll until you see the "TXT" record  that also contain the flag. 

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/e032a630-315f-4594-be64-e7d1762f686b)


3. GeoGuessr IRL 

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/43fa07db-971a-425d-b1a9-99bde0f67842)

* download the give "misc3.zip" 
* Open and you will get one picture. 

![the_photo](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/c62d7411-0e1c-4bf0-9f4e-bda854b87b1e)

* Using reverse image or google lens, to detect what is the location in the picture. 
* And you will get it, it is "Brooklyn bridge". 
* Open the https://what3words.com/ , and search brooklyn bridge". 
* Use Satelite view so, it will make it more viewable. 
* The provided is "h is the first letter for the first word" 
* Keep searching every square until you found the flag. 

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/5bce0a60-b9ce-441e-8f37-cb15957de67c).


* flag is ctf{happen.system.privately}


**Category : Web** 

1. Blank space - I mean Page 

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/1f3791ee-c4f6-4dbb-8d3b-ea4e886ac504)

* Visit the link given in the problem statement and it is just a blank page. 

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/6d43facd-9476-4db6-92d3-6b0f9d4eff17)

* The first think that come to my mind when come to a blank page, is robots.txt or source code 
* Lucky for me, when i search for the robots.txt file. I got this : 

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/e01043fe-7b07-44fe-8012-736969557e77)

* {/very-secretly-hidden}, let put in the url shall we? https://bxmweb1.jonathanw.dev/very-secretly-hidden/. 
* Boom ! you get the flag. 

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/46225df6-25ba-472e-b086-22e1fc48079e)


2. Respository Security 

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/5272771b-60d6-43a2-be59-decefa975a82)

* The website provided when you launch the instance is just a website to login. you need to find the credentials.
* To find the credentials, Download the web2.zip file provided.
* Once you opened the web2.zip file, it will contain a few file : 

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/bcfd174e-f1d0-49e0-ad9d-2e4a6e7e76b8)

* Let investigate all of the file and code, who knows it will contain the credentials.
* On file called "app.py", you can see at the line 5, state my_users and have a list of username and password and roles : 

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/6d969547-697b-44f0-a362-411c286f3bdf)

* Let try to use it, to log in into the web 
* Here i use username : chuck and password : norris. 
* Boom! succesful to login, then happily click the secret page on the nav bar of the website and you can view the flag

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/b48a3735-8728-4905-a932-9e8984ac39fc)

**Category : Crypto**

1. I can't Believe it

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/1fd491bd-6c64-47d2-865d-2191f4edc398)

* Given a file "cryp1.zip" 
* Download the zip file 
* and you can see poetry.txt
* open the 'txt' files and you can see a poetry.

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/1f25b734-8b0a-4fac-bc88-2a139a0cd857)

* The flag is already there, how? read the first letter work every lines. 
* And you can get "K N O W N C T F A L L", and then sort it, since our flag format is ctf{}, let sort the word that we got, we'll get ctf{allknown}.


2. Where snakes die. 

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/b93989d3-a01c-4b46-be1f-dd097cd946c6)

* Give a file "crypto2.zip".
* Download the zip files.
* you'll get clue.txt inside it.

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/d87916a2-c445-4035-8b9f-c16ce345bdb1)

* To find the flag, do you ever heard "Whitespace"?, this is a website that provide whitespace compiler : https://ideone.com/l/whitespace
* Copy and paste the clue.txt inside the whitespaces compiler and you can see the hidden symbol. 

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/7b42028c-3941-47a8-aedc-755c68c73dda)

* In whitespace format, "Tab: is for "-" and "Space" is for ".". 
* It seem like a morse code right? 
* Let move on to the morse translator.
* Change the "|" to "/" and the "-" to "_" 
* And finally you will get the flag 

flag = ctf{tabsoverspaces}


**Category : Forensic**


1. Selfie. 

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/5694867c-d7ad-4202-91c0-a05be4fc8002)

* Download the file foren1.zip
* Opened it and you will obtained a selfie picture.

![BxMCTF-Foren-1](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/0ad16a99-540c-4a52-a5f0-ecbd39833d7e)

* Use Exif data tools. to extract the data of the image.
* When the result come out, keep scrolling and investigate the data. 
* Then you will see at the "Licences" segment, it seem like something has been ecnrypted. 

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/c1cbfab8-2843-4810-b5b1-0062f3255008)

* Let try to decrypt the "Y3Rme25xaUoyQnQyaVZEa2d6fQ" using base64.
* Boom !! you get the flag.

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/b4a89996-6f3b-4de5-b7a7-7be787019866)



2. Street View

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/47e4de7d-72a6-4dd0-842c-e17eced3161c)

* Download the Foren2.zip 

* You will get an image 

![BxMCTF-Foren-2](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/6d82ad7b-9e34-426f-a820-f5efa8812223)

* Use Exif tools to view the image data

* In the meta data you can see you valuable information, which the longitude and latitude.

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/56d79ace-2dec-410d-b2a5-85be28cd5da8)

* Open google map and search using the infromation.

* It will bring you to the location 

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/fccf3897-e4bb-4031-93b5-e5dd6a2c305b)

* in the problem statement, state that the format of the flag is the building domain : ctf{domain}

* Use street view so that, it will make your investigation more easy. 

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/5b15277b-bffc-407c-8dfb-30d30e4b2faf)

* You can see that the location bring you to the Wallmart supermarket. 

* to find the wallmart supermarket domain, you can view the wallmart details. 

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/6f237087-03f7-4b4e-83d5-c0b951413dd8)

* There is the domain. 

![image](https://github.com/zer00neops/BxMCTF2023Writeup/assets/103404282/e55e79e0-a079-4af2-84e2-a78c2ac41cdc)

* Wrap the domain with ctf{} and you got the flag : ctf{walmart.ca}









