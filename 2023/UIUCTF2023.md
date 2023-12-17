**Event : Sat, 01 July 2023, 08:00 MYT — Mon, 03 July 2023. Organizer: SIGPwny**

<p align="center">
  <img src="https://ctftime.org/media/cache/3f/97/3f97a83ec8cf8013006ebb2342b7e9d3.png" width=300>
</p>

**[Category] OSINT [All Solved]**

**1. Finding Artifact 1**

![image](https://github.com/01bst/UIUctf2023/assets/103404282/fb0e6800-65bc-4345-a53d-0945f95b3c19)

* From the challenge card and challenge description has provided us with hints which is :

![image](https://github.com/01bst/UIUctf2023/assets/103404282/4f6b6ce9-0dab-410c-9595-e67f40963df5)

* For me, the hint is helpfull but there also lot of statue that can be resemble the hints. 
* Using the hints provided, i use ChatGPT to make the scope much smaller.
* Try and error using chatgpt, you will get 2 statue which is the Maitreya Buddha and Mahatma Gandhi statue. But between this two statue, only Maitreya buddha statue that located inside a museum.

![image](https://github.com/01bst/UIUctf2023/assets/103404282/b1c75221-d063-47d0-b4e3-b9181d24b2e8)

* Get the museum name and you wil get the flag which is UIUctf{museum_name}

**2. Finding Artifact 2**

![image](https://github.com/01bst/UIUctf2023/assets/103404282/e02f77ec-fabb-4d19-bee5-030e0a451618)

* For this challenge, i just walking around the internet as luckily i found this post on facebook.

![image](https://github.com/01bst/UIUctf2023/assets/103404282/08feb0b1-4aeb-4883-b540-5af694134417)

* And using the format uiuctf{museum_name}. Boom! i solve it.

**3. What For Dinner?**

![image](https://github.com/01bst/UIUctf2023/assets/103404282/8d8ea6ca-2cdf-4cfa-a17c-3323d7df57e5)

* For this challenge, for me, the hint provided is not so usefull since that not even lead to the flag.
  
* But another things that attract me is the text "find out that he uses a well known social network and and loves documenting his travels and reviewing his food. Find his online profile".
  
* Social network? Profile?. This is the absolutely hint that we need. Social network is social media, and most of people will share their adventure or anything on twitter or instagram. And profile here must mean that the user profile inside the social network. Nice! Let start OSINT-it.
  
* Inside the challenge description also provided the name which is "Jonnah Explore", so like try to find that username, luckily for me, i found the profile with exaclly the name on tiwtter.
  
* Click the profile and view the post. Boom here is the flag!

![image](https://github.com/01bst/UIUctf2023/assets/103404282/7659dac5-00ae-45b8-a157-1a1dc13128bb)



**4. Finding Jonnah?**

![image](https://github.com/01bst/UIUctf2023/assets/103404282/93cc92c6-6aa6-47a9-b101-05d67771a9c1)

* Download the image provided : Chicago.jpeg

* In this challenge, it ask us to find in which hotel does jonnah stay. Now, in this challenge is the hint provided is usefull, When you translate "joy" to Italy, you will get "Gioia". Fyi, there is a italian restaurant in west loop chicago called "Gioia Chicago".

* So the first thing that come to my mind is, the hotel where Jonnah stay must be near with the restaurant location, with this, it help to make the job scope smaller.

* Open the image provided.

![chicago](https://github.com/01bst/UIUctf2023/assets/103404282/94f756d4-ee50-4f88-ad88-6f3409116fc0)

* Use reverse image, and start using google map and google and anylyze the place.

* After a few minute struggling, i found the exactly hotel with exact view in the picture using google map.

![image](https://github.com/01bst/UIUctf2023/assets/103404282/ee3a3661-3a7d-4b8c-a938-adcfb15b5c16)

* Using the flag format uiuctf{hotel_name_inn} and Boom You solve it.
  

**5. Jonnah Journal?**

![image](https://github.com/01bst/UIUctf2023/assets/103404282/d511a244-78d8-47fa-9122-5463cc292b7d)

* In this challenge, usinf the hint provided, you can see that, all of it mentions the features in Github.

* And the text "His usernames have been relatively consistent", shows that, Jonnah use the same username like this twitter.

* Head out to Github and let find, his github account. Yup Found it, view the respo and you will something.

![image](https://github.com/01bst/UIUctf2023/assets/103404282/d5098720-9ece-4f15-b327-700e2d97f687)

* At first, i though the flag is China but, nah, this is to easy. When I try to input it as flag, it wrong. Then refer back to the hint. Github have a lot of features, let try it.

* First we view the branch, and yah there is something there.

![image](https://github.com/01bst/UIUctf2023/assets/103404282/5f27f1b0-f507-45a2-9f11-3d89f2927d0b)

* Keep viewing the branch, and you will find something usefull.

![image](https://github.com/01bst/UIUctf2023/assets/103404282/39620810-8d96-4ae6-8502-9edcd9097383)

* Based on it, i think it is italy. Using the flag format uiuctf{country_name} andd Boom!! solved it :D. 


**6. First class mail**

![image](https://github.com/01bst/UIUctf2023/assets/103404282/266f5c32-d263-47a8-b5ff-422ec953f3d2)

* For this challenge, it want us to find the zipcode in where he is located right now.

* In previous challenge, the "Finding Jonah" , it show that he stay at the hotel right? and we already found the hotel, so that mean he's there.

* View the address of the hotel that we found just now, use the zip code.

![image](https://github.com/01bst/UIUctf2023/assets/103404282/8e11f779-18df-4cd4-b17d-083228d0a0be)

* Boom We got it!!


