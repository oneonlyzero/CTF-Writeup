**Event : Sat, 15 July 2023, 09:00 MYT — Wed, 19 July 2023 | Oragnizer : les amateurs de la competition ctf**


<p align="center">
   <img src="https://github.com/01bst/CTF-Writeup/assets/103404282/93f73280-da61-4a54-9204-09d2d62fb8c8" width=300>
">
</p>

**[Category] OSINT**

**1. Gitint 5e**

* Talking about `Respo` will lead us to the github cause `respo = respository`, and meanwhile in the description already mention the username for the `respo` which is `les-amateurs`
  
* Go to `Github` and let try to find the username `les-amateurs`. You will get this github account :
  
* Go to `respo : more-CTFd-mods`

* To solve this challenge, you have to use every features in GitHub such as `Branch`, `Tree`, `Commit` and etc, So to find the flag for the this challenge is View all the `commit` done to the respo.

* View each changes done in the `commit`(recommended to start from bottom), and yup, inside the bottom(which is also the first) `commit`. You will get the first half of the flag : `amateursCTF{y0u-fOunD_m3`.

* To find the another half, continue to look all the `commit` file. And yup found it : `bu7:d1D U r34L!y?}`

* Combined it you will get the full flag : `amateursCTF{y0u-fOunD_m3bu7:d1D U r34L!y?}`, may use the Sha256 hash provided to check either your flag is true or false.

**2. Ginit 7d**

* Based on the challenge `Note` it has mentioned about `Pastebin` password bruteforcing warning. So the first thinks we need to find is the `Pastebin` file or link.

* Therefore, using the same GitHub `les-amateurs` and respo (`more-CTFd-mods`), Let try using other GitHub features. After using `Commit`, and `Branch`, still not get anything.

* I try to view the `respo issue`. The things that caught my eyes is `✔️ 1 closed` which mean 1 issue has been closed.
  
* Let try viewing the `closed issue`. Click the `closed issue`, then you will see 2 comment or conversation inside it.

* The second comment seem sus since it give a `link` and talk about `password`. So when click the [Link](https://pastebin.com/VeTDwT09), we get a locked `pastebin` file which is it is the exactly things that we want.

* Next is to find the `pastebin` password. Let keep looking inside the respo, got nothing left inside the `Issue`, so let try `Pull Request` and there is also `✔️1 closed` inside the `pull request`.

* Let try viewing it, yup another comment/conversation. Seem like they talk about `password`. But there is nowhere insight of the `password`.

* Seem like the conversation have been `Edited`. Luckily we can view the history of the `edited` text. in the `edit history` for the first conversation, he said `What's the password, is it like password123456 or something?` and the `edit history` for the second  conversation said `shhhh don't tell them.`.

*   So using the passowrd `password123456`, let try to opend the `locked pastebin` file.

*   And yup we unlocked it and received the flag

Flag : `amateursCTF{programs have issues, as do weak passwords}`


**3. ScreenshotGuesser**

* Gave to us 2 files  `Sceenshot.png`, and `main.py`, downloaded it and view the `screenshoy.png`. all you can see is a list of wifi, and the author want us to find the `coordinate` based on the wifi. 

* Here i use the [Wigle.net]([https://pastebin.com/VeTDwT09](https://wigle.net./)https://wigle.net./). which is a website that can help us to find the wifi location based on the `SSID`.

* Once you open the website, click on the `Advance Search` -> `General Search`.

* In the search filter, fill in the `search SSID / Network Name (exact match)` and  `SSID / Network Name (wildcards1: % and _):` with the wifi name that available inside the `screenshot.png`

* I always start from bottom :D, so let go use the bottom wifi name first which is `PRIMAVERA FOUNDATION 5G_2.4GEXT`, then click `query` to search.

* You will get a result that show the network `name` and also `coordinate` of the netwrok (Luck it was only 1 result :D)

* Using the `coordinate` in the search result, launch the instance provided inside the challenge `nc amt.rs 31450`, and submit the `coordinate`.

Flag : `amateursCTF{p0int_m4ster}`


**4. Archieved**

* The first things that come to my mind is `Web? Archived? = wayback machine` when i try using the `wayback machine`, I got nothing, hmm the author build diff.

* But we have another ways which is use [Archive.org](https://archive.org/) an library to achieve file, web and etc.

* I thought on searching for the CTF url and yup got nothing at first 😅, but came with an idea to search for the CTF name only which is `AmateursCTF`, select on `search metadata`

* OOOO we got something, 1 result, the title is `Archieved challenge` tho. Let try to open it.

* Inside the `archieved challenged`, you will 2 download option `7Z` and `Torrent`, let download using `7Z`. Once downloaded, view the zip file and you can see `flag.txt`

* Open the `flag.txt`

Flag : `amateursCTF{arch1v3d_r1ght_b3f0r3_th3_start}`.


**[Category] Forensic**

**1. Painfully Deep Flag**

* Download the provided `flag.pdf` file.

* Make sure to save the pdf file in directories which easier to find, then Use `pdftohtml <file name>` to change the pdf into html. 

* Once you executed it, all of the output containt of  `html scipt`, and `Images` will be save in the same folder/directories.
  
* View each of the image and you wil get the flag

Flag : `amateursCTF{0ut_0f_b0unds}`


**2. Zipper**

* Download the `flag.zip`, and using terminal, use `strings flag.zip | grep amateurs` to grep any strings inside the file that start with `amateurs`, and yups we get the first part of the flag : `amateursCTF{z1PP3d_`

* Then use `zipnote <file name>` which to view any comment inside our zip file. and yup there is our part 3 flag : `laY3r_0f`

* As you can see in `zipnote` output inside the rtermianl, there is a directory/file that seem sus, which is `/flag/flag201.txt`. why? because other `flag.txt` has been sorted ascending but only that directory/file at the top of the list. so let try to view what inside it using `unzip -p <zip file> <file path>`. Yup we got our part 4 flag :  `_Zips}`

* Seem like part 4 is the end of the flag, so we have to find the left part which is `part 2`, to find `part 2`, still referring to the the above `zipnote` output, you can see another sus things which is `flag/` directory which has been called twice. let view what inside it using the `unzip -p` command. Yup we got the part 2 of our flag : `in5id3_4_`

Flag : `amateursCTF{z1PP3d_in5id3_4_laY3r_0f_Zips}`


**[Category] Web**

**1. Latek**

* Open the website given inside the challenge description.

* Seem like a `Latex` language code, so let do `Latex Injection` 😄

* Take noted, the flag is in `/flag.txt`. so let do it.

* Using this script `\documentclass{article}\usepackage{verbatim}\begin{document}\verbatiminput{/flag.txt}\end{document}`

* Got it, Super EZ

Flag : `amateursCTF{th3_l0w_budg3t_and_n0_1nstanc3ing_caus3d_us_t0_n0t_all0w_rc3_sadly}`

**[Category] Misc**

**Insanity Check**

* Common sense is the main ingrediant for this challenge, first looking at the `chall description`, in the first sight you will see that is only a bunch of text start with `i` letter, but if you examining it carefully, there are few word that not start with `i`, let break it.

* Once done examining in you will get the word, `something`, `hidden`, `the`, `rules`. So this word lead us to `rules` which has been stated in the CTF discord channel.

* (Dont mind the flag :p it for another challenge.) So as you can see there is nothing left that you can mark as a flag. The things you have to do is `copy` the rules using the 

* Paste it anywhere and view it, you can see `number` that come before each text. let take that number.

* `107122414347637`, `125839376402043`, `122524418662265`, `12254990240549`, `121377376789885`. Hmm look like a decimal encryption but when try to decode it we got nothing.

* So First We need to change this `decimal` to `hexadecimal` 1 by 1 and then from `hexadecimal` to `ascii`.

* Yup got the flag : `amateursCTF{oops_you_found_me}`







