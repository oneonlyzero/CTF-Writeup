<p align="center">
   <img src="https://github.com/01bst/CTF-Writeup/assets/103404282/93f73280-da61-4a54-9204-09d2d62fb8c8" width=200>
">
</p>


Straight to the point writeup for another OSINT,Forensic, Web, and Misc challenge solved : By Zer00ne(Me) 

**Category: OSINT**

**1. Gitint 5e**
   
![Screenshot 2023-07-20 193326](https://github.com/01bst/AmateursCTF2023/assets/103404282/99fe3d98-904b-4f28-a648-6592b8aae68d)

* Talking about `Respo` will lead us to the github cause `respo = respository`, and meanwhile in the description already mention the username for the `respo` which is `les-amateurs`
  
* Go to `Github` and let try to find the username `les-amateurs`. You will get this github account :
  
![image](https://github.com/01bst/AmateursCTF2023/assets/103404282/6e50bc02-0902-42a9-80c1-78be6551824c)

* Go to `respo : more-CTFd-mods`

![image](https://github.com/01bst/AmateursCTF2023/assets/103404282/e62aaa2f-2347-4731-ab5d-195a2bba027c)


* To solve this challenge, you have to use every features in GitHub such as `Branch`, `Tree`, `Commit` and etc, So to find the flag for the this challenge is View all the `commit` done to the respo.

![image](https://github.com/01bst/AmateursCTF2023/assets/103404282/3b812aa2-30bd-4dbb-bcaf-92156d169ab4)

* View each changes done in the `commit`(recommended to start from bottom), and yup, inside the bottom(which is also the first) `commit`. You will get the first half of the flag : `amateursCTF{y0u-fOunD_m3`.

![image](https://github.com/01bst/AmateursCTF2023/assets/103404282/377ab18e-af91-43c1-9b0b-e38fb1833b58)


* To find the another half, continue to look all the `commit` file. And yup found it : `bu7:d1D U r34L!y?}`

![image](https://github.com/01bst/AmateursCTF2023/assets/103404282/b8e3cde6-c039-462e-a6ee-07ba23f0f5b2)

* Combined it you will get the full flag : `amateursCTF{y0u-fOunD_m3bu7:d1D U r34L!y?}`, may use the Sha256 hash provided to check either your flag is true or false.

**2. Ginit 7d**

![Screenshot 2023-07-20 193335](https://github.com/01bst/AmateursCTF2023/assets/103404282/d481e88a-e7c8-4f7a-96a5-23b35a0a9352)


* Based on the challenge `Note` it has mentioned about `Pastebin` password bruteforcing warning. So the first thinks we need to find is the `Pastebin` file or link.

* Therefore, using the same GitHub `les-amateurs` and respo (`more-CTFd-mods`), Let try using other GitHub features. After using `Commit`, and `Branch`, still not get anything.

* I try to view the `respo issue`. The things that caught my eyes is `✔️ 1 closed` which mean 1 issue has been closed.
  
![image](https://github.com/01bst/AmateursCTF2023/assets/103404282/d2ce6067-88e2-4ea8-b9b4-c689c2a7ff21)

* Let try viewing the `closed issue`. Click the `closed issue`, then you will see 2 comment or conversation inside it.

![image](https://github.com/01bst/AmateursCTF2023/assets/103404282/168b5c04-819e-4e03-a9a2-d8e5d3f7680d)

* The second comment seem sus since it give a `link` and talk about `password`. So when click the [Link](https://pastebin.com/VeTDwT09), we get a locked `pastebin` file which is it is the exactly things that we want.

![image](https://github.com/01bst/AmateursCTF2023/assets/103404282/2e0727d8-cd09-454f-8b68-d1230fff6eb8)

* Next is to find the `pastebin` password. Let keep looking inside the respo, got nothing left inside the `Issue`, so let try `Pull Request` and there is also `✔️1 closed` inside the `pull request`.

![image](https://github.com/01bst/AmateursCTF2023/assets/103404282/b45ec2ff-638c-4634-9f3e-1a20e3ab453b)

* Let try viewing it, yup another comment/conversation. Seem like they talk about `password`. But there is nowhere insight of the `password`.

![image](https://github.com/01bst/AmateursCTF2023/assets/103404282/9f62a796-ec9f-495d-a429-020f8dad6349)

* Seem like the conversation have been `Edited`. Luckily we can view the history of the `edited` text. in the `edit history` for the first conversation, he said `What's the password, is it like password123456 or something?` and the `edit history` for the second  conversation said `shhhh don't tell them.`.

*   So using the passowrd `password123456`, let try to opend the `locked pastebin` file.

*   And yup we unlocked it and received the flag

![image](https://github.com/01bst/AmateursCTF2023/assets/103404282/720827a5-733d-47a5-90cb-239861fee384)

Flag : `amateursCTF{programs have issues, as do weak passwords}`


**3. ScreenshotGuesser**

![Screenshot 2023-07-20 193342](https://github.com/01bst/AmateursCTF2023/assets/103404282/0e2da08b-9769-462f-ba55-7f3886708823)

* Gave to us 2 files  `Sceenshot.png`, and `main.py`, downloaded it and view the `screenshoy.png`. all you can see is a list of wifi, and the author want us to find the `coordinate` based on the wifi. 

![image](https://github.com/01bst/AmateursCTF2023/assets/103404282/2d424321-7913-4d9f-9901-ade7b6452c4f)

* Here i use the [Wigle.net]([https://pastebin.com/VeTDwT09](https://wigle.net./)https://wigle.net./). which is a website that can help us to find the wifi location based on the `SSID`.

* Once you open the website, click on the `Advance Search` -> `General Search`.

![image](https://github.com/01bst/AmateursCTF2023/assets/103404282/d4d94b83-5385-487b-ba47-6a7e565a07ac)


* In the search filter, fill in the `search SSID / Network Name (exact match)` and  `SSID / Network Name (wildcards1: % and _):` with the wifi name that available inside the `screenshot.png`

* I always start from bottom :D, so let go use the bottom wifi name first which is `PRIMAVERA FOUNDATION 5G_2.4GEXT`, then click `query` to search.

* You will get a result that show the network `name` and also `coordinate` of the netwrok (Luck it was only 1 result :D)

![image](https://github.com/01bst/AmateursCTF2023/assets/103404282/0f1000db-a5dd-4dd3-9763-2f121901696a)

* Using the `coordinate` in the search result, launch the instance provided inside the challenge `nc amt.rs 31450`, and submit the `coordinate`.

Flag : `amateursCTF{p0int_m4ster}`


**4. Archieved**

![Screenshot 2023-07-20 193350](https://github.com/01bst/AmateursCTF2023/assets/103404282/907dd565-10ec-49ba-984c-ec81c1953b2c)

* The first things that come to my mind is `Web? Archived? = wayback machine` when i try using the `wayback machine`, I got nothing, hmm the author build diff.

* But we have another ways which is use [Archive.org](https://archive.org/) an library to achieve file, web and etc.

![image](https://github.com/01bst/AmateursCTF2023/assets/103404282/a6e164a2-7ef4-4712-9090-8e2b90b3214d)

* I thought on searching for the CTF url and yup got nothing at first 😅, but came with an idea to search for the CTF name only which is `AmateursCTF`, select on `search metadata`

* OOOO we got something, 1 result, the title is `Archieved challenge` tho. Let try to open it.

![image](https://github.com/01bst/AmateursCTF2023/assets/103404282/c5be2d02-04b4-47d2-9b90-f946f74ff602)

* Inside the `archieved challenged`, you will 2 download option `7Z` and `Torrent`, let download using `7Z`. Once downloaded, view the zip file and you can see `flag.txt`

* Open the `flag.txt`

Flag : `amateursCTF{arch1v3d_r1ght_b3f0r3_th3_start}`.


**Category : Forensic**

**1. Painfully Deep Flag**

![Screenshot 2023-07-20 193258](https://github.com/01bst/AmateursCTF2023/assets/103404282/148afad4-648b-4a93-85cd-b0603a9df6e0)

* Download the provided `flag.pdf` file.

* Make sure to save the pdf file in directories which easier to find, then Use `pdftohtml <file name>` to change the pdf into html. 

* Once you executed it, all of the output containt of  `html scipt`, and `Images` will be save in the same folder/directories.
  
* View each of the image and you wil get the flag

Flag : `amateursCTF{0ut_0f_b0unds}`


**2. Zipper**

![Screenshot 2023-07-20 193306](https://github.com/01bst/AmateursCTF2023/assets/103404282/9b23f885-f930-480c-8ae1-04d8a1377b14)

* Download the `flag.zip`, and using terminal, use `strings flag.zip | grep amateurs` to grep any strings inside the file that start with `amateurs`, and yups we get the first part of the flag : `amateursCTF{z1PP3d_`

* Then use `zipnote <file name>` which to view any comment inside our zip file. and yup there is our part 3 flag : `laY3r_0f`

* As you can see in `zipnote` output inside the rtermianl, there is a directory/file that seem sus, which is `/flag/flag201.txt`. why? because other `flag.txt` has been sorted ascending but only that directory/file at the top of the list. so let try to view what inside it using `unzip -p <zip file> <file path>`. Yup we got our part 4 flag :  `_Zips}`

* Seem like part 4 is the end of the flag, so we have to find the left part which is `part 2`, to find `part 2`, still referring to the the above `zipnote` output, you can see another sus things which is `flag/` directory which has been called twice. let view what inside it using the `unzip -p` command. Yup we got the part 2 of our flag : `in5id3_4_`

Flag : `amateursCTF{z1PP3d_in5id3_4_laY3r_0f_Zips}`


**Category : Web**

**1. Latek**

![Screenshot 2023-07-20 190703](https://github.com/01bst/AmateursCTF2023/assets/103404282/c73aae6b-8e1d-4de9-acd9-28088d0c4053)


* Open the website given inside the challenge description.

![Screenshot 2023-07-20 190739](https://github.com/01bst/AmateursCTF2023/assets/103404282/f6bf398f-1ff4-4dd0-b138-182f178a755e)

* Seem like a `Latex` language code, so let do `Latex Injection` 😄

* Take noted, the flag is in `/flag.txt`. so let do it.

* Using this script `\documentclass{article}\usepackage{verbatim}\begin{document}\verbatiminput{/flag.txt}\end{document}`

* Got it, Super EZ

![Screenshot 2023-07-20 190904](https://github.com/01bst/AmateursCTF2023/assets/103404282/15b86e4e-0348-4cfb-8905-2e4b576ec0c1)


Flag : `amateursCTF{th3_l0w_budg3t_and_n0_1nstanc3ing_caus3d_us_t0_n0t_all0w_rc3_sadly}`

**Category : Misc**

**Insanity Check**

![Screenshot 2023-07-20 191113](https://github.com/01bst/AmateursCTF2023/assets/103404282/07c530e4-390e-4613-9d23-128745902bec)

* Common sense is the main ingrediant for this challenge, first looking at the `chall description`, in the first sight you will see that is only a bunch of text start with `i` letter, but if you examining it carefully, there are few word that not start with `i`, let break it.

* Once done examining in you will get the word, `something`, `hidden`, `the`, `rules`. So this word lead us to `rules` which has been stated in the CTF discord channel.

![Screenshot 2023-07-20 191452](https://github.com/01bst/AmateursCTF2023/assets/103404282/180170a2-3a27-42a4-9e3c-5db5400ed2dc)

* (Dont mind the flag :p it for another challenge.) So as you can see there is nothing left that you can mark as a flag. The things you have to do is `copy` the rules using the 

![Screenshot 2023-07-20 191728](https://github.com/01bst/AmateursCTF2023/assets/103404282/8811b5f7-5089-43ab-9abd-0bcfc055782f)


* Paste it anywhere and view it, you can see `number` that come before each text. let take that number.

![Screenshot 2023-07-20 191812](https://github.com/01bst/AmateursCTF2023/assets/103404282/6f96265a-28e0-4bb2-a943-ef2afe686e05)

* `107122414347637`, `125839376402043`, `122524418662265`, `12254990240549`, `121377376789885`. Hmm look like a decimal encryption but when try to decode it we got nothing.

* So First We need to change this `decimal` to `hexadecimal` 1 by 1 and then from `hexadecimal` to `ascii`.

* Yup got the flag : `amateursCTF{oops_you_found_me}`







