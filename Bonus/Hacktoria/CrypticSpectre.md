<h1>
  OSINT : CrypticSpectre - Medium
</h1>

**Badge** 
> Zeroo

<p align="center" width=300>
  <img src="https://github.com/user-attachments/assets/7c6bfaba-bac3-4bbe-946a-cc9fa98f34e8" width=300>
</p>


**Mission [Get full Materials at [G Drive](https://drive.google.com/drive/folders/12qyPNwlnsxpGB0E_Sp5VSQAsKj-1C_KG)]**

```
Greetings, Special Agent K.

We’ve received intel about a recent cyber attack on a high-profile organization. Our analysts have provided us with a malware hash found during the investigation:

9e7053a4b6c9081220a694ec93211b4e

Your mission, should you choose to accept it, is to analyze this hash and determine the Advanced Persistent Threat (APT) group behind it and the target of their attack.

As always, Special Agent K. The Contract is yours, if you choose to accept.


```

**Material**

```
Malware Hash: 9e7053a4b6c9081220a694ec93211b4e
```

**Answer Instruction**

```
Answer format: APTgroupnumber_targetoftheattack

Answer example: APT43_departmentofjustice

```

**Solution**

```
1. Use virus total to analysis the hash, go through the relation and community mentioned, a lot of them mentions Fancy Bears (Threat Actor Group)

2. Search for Fancy bears in google, i found a website that explain a few details of this group, from the headline (https://www.radware.com/cyberpedia/ddos-attacks/fancy-bear-apt28-threat-actor/), i got the first part of the answer which is the APT group (APT28)

3. Then use Hybrid Analysis website to find another information we can find regarding the hash (https://www.hybrid-analysis.com/sample/4845761c9bed0563d0aa83613311191e075a9b58861e80392914d61a21bad976?environmentId=120), in one of the section is the section in the analysis which is Additional context 
i found a few refference link that bring us to the blog of the attack (https://www.threatconnect.com/tapping-into-democratic-national-committee/)

4. The answer is APT28_democratnationalcommittee
```
