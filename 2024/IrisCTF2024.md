**Event :Sat, 06 Jan. 2024, 08:00 MYT — Mon, 08 Jan. 2024 | Oragnizer : IrisSec**


<p align="center">
   <img src="https://ctftime.org/media/team/iris-zoomed.jpg" width=300>
</p>

**[Category] Forensic**

**1. Not Just Media**

* Download the zip file gave in the chall description and unzip it will get you a mkv file set as `chal.mkv`

* First, using `mkvtools`, im using the command `mkvinfo` to view all of the info regarding the `chal.mkv`.

* in the info output, you can saw a few tracks and attachment embeded inside the `chal.mkv`.

* Next, using `mkvextract` command to extract the track and attachments file.

* Tracks including the `oroginal video`, `song audio` and `subtitles` file, meanwhile the attachments include 3 `.tff` file which is a font files.

* Next step, inside the chall description, it talk about `wrong subtittles.`, therefore im focus more to the `subtitles` track file it self.

* Opening the `sub` files, you can view the subtitles or dialouges involves which is a chinese word. Try to decode or translate the chinese word, you will ended up get nothing but a normal plain text.

* Move on to the solution, to obtain the flag, you can use one of the font attachments file that been extracted from the `chal.mkv` file using the web called `fontsee.com`, upload the font file, and paste the chinese word inside the preview box, you will obtain the flag. 
