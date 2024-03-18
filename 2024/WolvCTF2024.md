**Event :  Saturday, 16 March 2024, 07:00 AM MYT — Monday, 18 March 2024, 07:00 AM MYT | Oragnizer : WolvSec**<br>

**Appreciation: Congrats To The team for secure 23th from 300++ teams**


<p align="center">
   <img src="https://miro.medium.com/v2/resize:fit:300/format:webp/0*QjGHN8bu9hZIaz-n" width=200>
</p>


**Category : OSINT**

**1. WOLPHV I: Reconnaissance**

- Searching for "Wolphv Ransomware Group" on search engine will lead you to the the `X` post from the account `FalconFeeds.io`. [Here](https://twitter.com/FalconFeedsio/status/1706989111414849989)
- Take a look to all of the reply/comment inside the post you will notice the account with the username `Joe Osint` which seem to look like he commenting some `base64` text. [Here](https://twitter.com/JoeOsint__)
- Take the `base64` and decode it. you will successfully obtained the flag :).

**2. WOLPHV II: Infiltrate**

- Try to find others social media related to the `Wolvph` group beside their official `X` account and find one account related to them on `Facebook`. [Here](https://www.facebook.com/groups/921721029413388/?hoisted_section_header_type=recently_seen&multi_permalinks=921722342746590)
- In the `Facebook` account, you will find a video post, seem normal in the beginning, but at the end of the video, you can see all of the search tab on the top of browser right after the person close the slide.
- Looking at the search tab, you find a few searching for example `Funny cat`, `How to hack`, etc. but the one that caught my eye is the discord search : `discord.com/UbeJPeBT`.
- At first, if you directly just copied 100% like in the search, you go to the discord `unable to find channel page`.
- Just change the `.com` of the link to `.gg` and you will be directed to a discord channel `Wolpvh`
- Look at the top at the `General` chat and you will obtained the flag.
