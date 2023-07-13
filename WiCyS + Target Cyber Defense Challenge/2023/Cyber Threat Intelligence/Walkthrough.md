**1.**

![Screenshot 2023-07-13 013117](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/77c27b58-1af5-43af-9a12-790603f375bc)

Solving this challenge was relatively straightforward as it involved a simple lookup task. To identify the company associated with a specific IP address, I utilized the website https://lookup.icann.org/en. By inputting the IP address into the search function, I quickly obtained information about the company that owned that particular IP address.

`FLAG{Digital Ocean}`

![Screenshot 2023-07-13 013321](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/5ca61f5a-9d99-4058-8768-7b2a2ebf7d3f)

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

**2.**

![Screenshot 2023-07-13 014346](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/2ae16856-804a-4f9c-b2d7-13550f37c44c)

In order to analyze the suspicious command, I referred to the widely recognized MITRE Attack Framework. This framework serves as a comprehensive knowledge base, offering insights into various tactics, tools, and techniques employed by hackers. It has become an industry standard for categorizing and understanding the methodologies used by threat actors. Notably, the suspicious command I encountered was directly linked to a relevant page within the MITRE Attack Framework, providing valuable context and insights into its potential implications.

`FLAG{T1482}`

![Screenshot 2023-07-13 020603](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/b9bde5ae-f8d4-426f-be3d-156c6ab735ce)

-------------------------------------------------------------------------------------------------------------------------------------------------------------------
**3.**

![Screenshot 2023-07-13 021336](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/234cb4ad-85fa-4147-8173-a07de5c28fd1)

Upon examining the provided ISO file, I discovered that it contained multiple files. To delve deeper into the investigation, I decided to extract valuable information by running the "strings" command on all the files. During this process, while analyzing the contents of the version.dll file, I uncovered a noteworthy domain: shiniest.sting.example.

`FLAG{shiniest.sting.example}`

-----------------------------------------------------------------------------------------------------------------------------------------------------------------

**4.**

![Screenshot 2023-07-13 025048](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/b1ff2aba-fb98-42dc-943a-3112638e41fc)

This challenge required some exploration before reaching the flag. Initially, I faced uncertainty regarding the appropriate approach. I decided to run the "strings" command on all the files, hoping for a breakthrough. However, this led me down a rabbit hole for days.

I turned to VirusTotal for assistance. Through VirusTotal's analysis, I discovered a total of 20 domains associated with the challenge. To organize my findings, I jotted down all the domains on a notepad. Then, I carefully reevaluated the caption provided in the challenge repeatedly, seeking any clues or connections.

While pondering the term "cobalt," I drew a parallel to the color cobalt blue. Leveraging this insight, I narrowed down my focus to the domains that included the word "blue" within them. By methodically eliminating domains that didn't meet this criterion, I eventually discovered the flag, successfully completing the challenge.

`FLAG{blue.venom.sting.example}`

![Screenshot 2023-07-13 025437](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/e7400436-e13a-4be3-8f35-895d596e65c7)
---------------------------------------------------------------------------------------------------------------------------------------------------------------

**5.**

![Screenshot 2023-07-13 031527](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/a64a5283-aa29-4650-9aa4-f78ebf4a13e7)

During the challenge, we were given three files: a binary (bin) file and two encrypted flag text files. A crucial detail that emerged was that Shiny Scorpion ransomware group had copied code from an existing gang.

Upon observing the unusual "C_I_0P" extension, I did an extensive research and found that Shiny Scorpion copied from the CI0P group. Luckily, earlier iterations of their ransomware exhibited encryption weaknesses. As a solution, SentinelOne created a dedicated decryptor tool that could be obtained from: https://github.com/SentineLabs/Cl0p-ELF-Decryptor.

By using the ELF Decryptor tool from Sentine Labs, I effectively decrypted the sting.bin file by applying it to the "flag.txt.C_I_0P" text file. After executing this tool I finally found the flag.

`FLAG{maintain_offline_backups}`

![Screenshot 2023-07-13 035053](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/3b14a4dd-d6dc-47db-acce-7a19661523fb)



























