**Event :  Saturday, 16 March 2024, 07:00 AM MYT — Monday, 18 March 2024, 07:00 AM MYT | Oragnizer : WolvSec**<br>

**Appreciation: Congrats To The team for secure 23th from 300++ teams, Here i would like to share the OSINT Chall from the CTF mentioned.**


<p align="center">
   <img src="https://miro.medium.com/v2/resize:fit:300/format:webp/0*QjGHN8bu9hZIaz-n" width=200>
</p>


**Category : OSINT**

**1. WOLPHV I: Reconnaissance**

<p align="center">
   <img src="https://github.com/ItsZer01/CTF-Writeup/assets/103404282/194a5356-4594-4035-9f21-2b715558877c" width=400>
</p>

- Searching for "Wolphv Ransomware Group" on search engine will lead you to the the `X` post from the account `FalconFeeds.io`. [Here](https://twitter.com/FalconFeedsio/status/1706989111414849989)

<p align="center">
   <img src="https://github.com/ItsZer01/CTF-Writeup/assets/103404282/2b1fe70e-fc93-4ceb-a535-bc01356f3b64" width=400>
</p>

- Take a look to all of the reply/comment inside the post you will notice the account with the username `Joe Osint` which seem to look like he commenting some `base64` text. [Here](https://twitter.com/JoeOsint__)
- Take the `base64` and decode it. you will successfully obtained the flag :).

**2. WOLPHV II: Infiltrate**

<p align="center">
   <img src="https://github.com/ItsZer01/CTF-Writeup/assets/103404282/92050bc5-b92a-4d01-8e14-c48056f00406" width=400>
</p>

- Try to find others social media related to the `Wolvph` group beside their official `X` account and find one account related to them on `Facebook`. [Here](https://www.facebook.com/groups/921721029413388/?hoisted_section_header_type=recently_seen&multi_permalinks=921722342746590)

<p align="center">
   <img src="https://github.com/ItsZer01/CTF-Writeup/assets/103404282/aa03723a-8c33-4506-98bc-28a18f1f6826" width=400>
</p>

- In the `Facebook` account, you will find a video post, seem normal in the beginning, but at the end of the video, you can see all of the search tab on the top of browser right after the person close the slide.

<p align="center">
   <img src="https://github.com/ItsZer01/CTF-Writeup/assets/103404282/c9b49905-1569-4624-b282-4cd0347e1568" width=400>
</p>

- Looking at the search tab, you find a few searching for example `Funny cat`, `How to hack`, etc. but the one that caught my eye is the discord search : `discord.com/UbeJPeBT`.
- At first, if you directly just copied 100% like in the search, you go to the discord `unable to find channel page`.
- Just change the `.com` of the link to `.gg` and you will be directed to a discord channel `Wolpvh`
- Look at the top at the `General` chat and you will obtained the flag.

**3. WOLPHV III: p1nesh4dow48**

<p align="center">
   <img src="https://github.com/ItsZer01/CTF-Writeup/assets/103404282/7842a72b-36f7-4b44-8d6b-57e369ea2f5a" width=400>
</p>

- You will get an image of an apartment between the conversation.
- First, i enchance the image using `Ai image Enhancer` to make the imaage more cleaer.

<p align="center">
   <img src="https://github.com/ItsZer01/CTF-Writeup/assets/103404282/0b163cba-cb7e-4311-8ee9-6199b3aedf71" width=400>
</p>

- Then try to look any particular on the image that will help to make the searching scope became smaller.
- We obtained a few information in the image such as : The parking lot sign `Pine Ridge Visitor Parking`, The car driver on the left side (probally USA), And the apartment.
- Using a few osint tool `(google image, google maps, search engine)  and information gathered)`

<p align="center">
   <img src="https://github.com/ItsZer01/CTF-Writeup/assets/103404282/072a40c2-7e67-465d-8a0a-2ab0e19f97c7" width=400>
</p>

- You will find the location of the apartment which is `Pine Ridge Apartment` or `Marquette's Affordable Housing` located at  `Marquette Michigan`
- The flag, required you to find the exact long,lang of the image location and wrap it in the flag format : `wctf{xxxx,xxxx}`

**4. WOLPHV IV: d4wgbyte262**

- Inside the discord conversation, the user `d4wgbyte262` mentioned about his dog, and a little bit information of his house location `i live the closest to a fire station out of all my friends who are neighbors they dont understand my pain - d4wgbyte262 `

<p align="center">
   <img src="https://github.com/ItsZer01/CTF-Writeup/assets/103404282/c3036886-8bc9-43f7-8b92-1534b20627f2" width=400>
</p>

- Straight to the point after a few time searching, you will found an account with username `d4wgbyte262` on `flickr` a website to post image with a bunch of dog images, [Here](https://www.flickr.com/photos/200261418@N03/albums/)

<p align="center">
   <img src="https://github.com/ItsZer01/CTF-Writeup/assets/103404282/8e29006e-99a9-420c-9a42-878131d3db37" width=400>
</p>

- Checking each one of the image will also show the location of the image with the lang and long.
- Since there are so many images, you have to look and find which one is the nearest with a fire station, just like he mentioned in the discord.
- Take the long,lang and wrap it in the flag format `wctf{xxxx,xxxx}`


**5. WOLPHV V: luvh4ck573 (Late Solved)**

- First, looking at the conversion in the discord, luvh4ck573 say that `guys should i get pizza subway or mcdonalds theyre all so close to me - luvh4ck573`. We can use this as a hint. 
- In the chall description mentioned that `You do not need to make a dating profle`. We can use this to start our searching.

<p align="center">
   <img src="https://github.com/ItsZer01/CTF-Writeup/assets/103404282/52590670-aeb9-40d4-8af0-eda9e4772f26" width=400>
</p>

- On one of the famous dating app or website `Tinder`, you will find an account with the username `LuvH4ck573`. [Here](https://tinder.com/@luvh4ck573)

<p align="center">
   <img src="https://github.com/ItsZer01/CTF-Writeup/assets/103404282/d86599d8-07a0-4281-bb19-2c0c27187faa" width=400>
</p>

- Based on the tinder pfp you can see how this guys look likes, try to find more about this guys you will find his `tumblr` blog. [Here](https://www.tumblr.com/nathan-rizz-blog67945?redirect_to=%2Fnathan-rizz-blog67945&source=blog_view_login_wall)

<p align="center">
   <img src="https://github.com/ItsZer01/CTF-Writeup/assets/103404282/baf34195-8fd4-49e3-86a4-64a487259a5c" width=400>
   <img src="https://github.com/ItsZer01/CTF-Writeup/assets/103404282/11eed182-03da-4eae-b09d-8e7719646de9" width=400>
</p>

- Inside the tumblr, he share the link to a youtube video. [Here](https://www.youtube.com/watch?v=ZEJdSXbglZs) and a posting that said `i love public transit there is a bus stop outside my apartment `
- Using wayback machine tool, and search for the youtube link, you will find another snapshot was make for the link. In the old snapshot, you will find the `email address` on the video description.
- Find the handler name of the email address using the osint tool (epieos, etc)
- Got the name `nathaniel sterling`, try to find anything interesting with this name such as media social.

<p align="center">
   <img src="https://github.com/ItsZer01/CTF-Writeup/assets/103404282/37c68842-e72f-47b3-a406-9faeb5d3f85f" width=400>
</p>

- Find Instagram account with the name. [Here](https://www.instagram.com/nathaniel_sterling2/) 
- The bio of the instagram account stated that `hacker from Collingwood Ontario`.
- Using the hint or details we got from the searching to find the exact location `(Hint : pizza subway or mcdonalds theyre all so close to me, bus stop outside my apartment,  from Collingwood Ontario)`.
- Find the exact long and lang of the location and wrap it in the flag format : `wctf{xxxxx,xxxxx}`
