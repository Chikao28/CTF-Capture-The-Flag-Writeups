**1.**

![Screenshot 2023-07-12 170051](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/97c82ade-f84f-4f5e-a5fe-6b18a04058d4)

I used CyberChef and used the ROT13 cipher to dedode the string "GUR GNETRG UNF ORRA NPDHVERQ" and received the flag.

FLAG{THE TARGET HAS BEEN ACQUIRED}

![Screenshot 2023-07-12 170529](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/06eb5ee2-f7e4-431c-bbd6-b852da7beb4c)

----------------------------------------------------------------------------------------------------------------------------------------------------

**2.**

![Screenshot 2023-07-12 174528](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/576b79d7-5006-4a2e-aeab-32b178c6d0c9)

In this particular challenge, a questionable email arrives with an "attachment" containing a scorpion picture. Whenever a PNG file is included in a Capture The Flag (CTF) scenario, I find it beneficial to employ zsteg, a tool designed to reveal concealed information within png images.


![Screenshot 2023-07-12 175139](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/22fdcf72-eb8a-4b6f-8c78-2b8251dae559)

I ran zsteg and successfully extracted the Least Significant Bit (LSB) data: KaierljsipvgbediecsvhrrscaEvvqyq=====

Following the clues provided in the challenge description, I applied the Vigenère cipher to decrypt the string. Knowing that this cipher involves a key, I contemplated the possibility of another element concealing the key. Despite my thorough investigation, I couldn't locate any such component. As a last resort, I decided to try the name of the ransomware gang, "shinyscorpion," and to my delight, it turned out to be the correct key!

FLAG{StarttheransomwareattackonMonday}

![Screenshot 2023-07-12 210026](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/11a55ff6-17c1-4119-9de8-023f8c361c14)

---------------------------------------------------------------------------------------------------------------------------------------------------------

**3.**

![Screenshot 2023-07-12 180543](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/e0615219-77df-49f6-9b01-bc35efc9c3e1)

Let me start off by saying the title of this challenge turned out to be quite deceptive! It presented a seemingly harmless .txt file containing the renowned poem "Spellbound" by Emily Brontë.
Considering the surplus of blank spaces following the sentences, I conducted thorough research on stegonagraphy whitespaces. During my research, I stumbled upon stegsnow, a widely recognized tool that employs the technique of appending whitespace to hide ASCII text within a file. Given the snowy connotation of the title, it seemed obvious to give this tool a try. However, I ende up in a rabbit hole... Later I realized all I had to do was count the whitespaces and created a simple puthon script that automatically counts it for me.

After executing the script, the output consisted of decimal numbers. Recognizing their potential significance, I proceeded to convert them to ASCII characters. Through this conversion process, I discovered the flag hidden within the text!

FLAG{QU1X0T1CALLY}

![Screenshot 2023-07-12 184027](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/e4ffc565-a0db-40db-8298-defbc7f8b0c7)
![Screenshot 2023-07-12 185912](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/d6b1b109-f32b-41b9-9941-4ea1eb027275)

------------------------------------------------------------------------------------------------------------------------------------------------------------

**4.**

![Screenshot 2023-07-12 191348](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/40bf10d4-6760-4eff-a27a-b93c5ccdb7f4)

Upon initial inspection, the encoded message resembled Morse code, but upon closer examination, I noticed the word "bacon" written in red. This immediately triggered my familiarity with the Bacon cipher. Typically, the Bacon code employs either A's and B's or 0's and 1's (both variations are supported by default).

To decipher the message, I turned to the helpful online tool at https://www.cachesleuth.com/multidecoder/, which featured a Bacon decoder. Utilizing this tool, I successfully decoded the message and unveiled the flag!

FLAG{THEPLANISINPLACE}

![Screenshot 2023-07-12 193926](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/dc76e713-e4d0-4ff7-8f44-e31069b0bc70)

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

**5.**

![Screenshot 2023-07-12 195054](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/e6916275-497c-4bf3-ba32-6989a3e8482b)

This challenge revolved around a straightforward Diffie-Hellman key exchange problem. The provided text mentioned Alice requesting specific quantities of food items from Bob, including nine orders of papaya salad, seven orders of grape pastries, six dozen apples, and eight loaves of banana bread. The mention of "Director Diffie-Hellman" alluded to the renowned Diffie-Hellman Key Exchange algorithm.

To solve this challenge, I utilized a Diffie-Hellman calculator. By correctly inputting the prime number (P), ensuring the generator (G) was less than the prime number, and considering that private keys could be either 8 or 6, I performed the necessary calculations. Ultimately, this enabled me to uncover the flag and successfully complete the challenge.

FLAG{1}

![Screenshot 2023-07-12 195835](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/8ccb631b-1c3b-4ae3-b1b9-95055667164a)

-------------------------------------------------------------------------------------------------------------------------------------------------------------------




