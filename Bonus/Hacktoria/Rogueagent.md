

<h1>
  Foren-OSINT : Rogue Agent - Easy
</h1>

**Badge** 
> Zeroo

<p align="center" width=300>
  <img src="https://github.com/user-attachments/assets/0a907072-ffd0-4077-9efe-73500ae63926" width=300>
</p>


**Mission [Get full Materials at [G Drive](https://drive.google.com/drive/folders/1bJyerOJa-Ip9EeBTNH9tg8chtFHyPqF1)]**

```
Greetings Special Agent.

We have a request on our hands from our friends over at the CIA. In September of 2021, one of their operatives went missing in action. Upon further investigation, it was discovered this operative went rogue and started a smuggling business for the Russians. Mostly dealing in complex electronics, which have become difficult to come by for Russians after sanctions began.

The agent we’re looking for is named Valentino Maggi. Born in Brooklyn New York on 18.05.1987. Valentino is one of five sons of the Valentino family, who moved to the United States during World War II. Having grown up a middle class lifestyle, his father a car salesman and mother working as an elementary school teacher. Valentino was recruited into the CIA during his time as a student at Columbia University.

Most of his 10 years in active service were spent as an analyst working out of Langley. Recently though, in August of 2020, Valentino moved to oversees work. Being stationed in Italy as a liaison officer for the Italian foreign intelligence agency “Agenzia Informazioni e Sicurezza Esterna”.

Doing stellar work, right up until the point he went missing. Prompting an extensive investigation into his whereabouts. Documents were eventually found on his computer, recovered using forensics tools to recover deleted files. These indicate a heavy involvement with the Russian underground. Acquiring much needed microelectronics for the Russian government.

And that is where your task begins, Special Agent K. One of the files recovered from Valentino’s computer, is an image with a text file. We believe this to be the current location of Valentino Maggi. Locate the safehouse, so local authorities can raid the premises.

As always, the contract is yours, if you choose to accept.


```

**Material**
<p>
  <img src="https://github.com/user-attachments/assets/71d9032f-81a8-4453-a84f-a430faebe65f" width=300>
</p>


**Answer Instruction**

```
answer hint: country-town-coordinate
answer example: spain-madrid-12.345678-12.345678

```

**Solution**

```
1. Use strings command or strings -tail command to string out the hidden messages from the material, you will get encrypted text which is (Zhh\djrljhZdb\`jnphf).

2. Bake the encrypt text in cyberchef, use this recipe : Magic and turn on instrusive mode, from the various output you can obtain the coordinate (-44.259654-21.057843)

3. the "-" symbol in the coordinate that you get is not negative but "-" in the answer format, remove the "-" symbol and use that coor in google to find the location of the material.

4. Found the exact same location in the material, using the answer format we got the answer : serbia-rakinac-44.259654-21.057843

```

