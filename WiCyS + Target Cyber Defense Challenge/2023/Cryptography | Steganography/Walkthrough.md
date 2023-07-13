**1.**

![Screenshot 2023-07-12 170051](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/97c82ade-f84f-4f5e-a5fe-6b18a04058d4)

I used CyberChef and used the ROT13 cipher to dedode the string "GUR GNETRG UNF ORRA NPDHVERQ" and received the flag.
FLAG: {THE TARGET HAS BEEN ACQUIRED}

![Screenshot 2023-07-12 170529](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/06eb5ee2-f7e4-431c-bbd6-b852da7beb4c)

----------------------------------------------------------------------------------------------------------------------------------------------------

**2.**

![Screenshot 2023-07-12 174528](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/576b79d7-5006-4a2e-aeab-32b178c6d0c9)

In this particular challenge, a questionable email arrives with an "attachment" containing a scorpion picture. Whenever a PNG file is included in a Capture The Flag (CTF) scenario, I find it beneficial to employ zsteg, a tool designed to reveal concealed information within png images.


![Screenshot 2023-07-12 175139](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/22fdcf72-eb8a-4b6f-8c78-2b8251dae559)

I ran zsteg and successfully extracted the Least Significant Bit (LSB) data: KaierljsipvgbediecsvhrrscaEvvqyq=====

Following the clues provided in the challenge description, I applied the Vigenère cipher to decrypt the aforementioned string. Knowing that this cipher involves a key, I contemplated the possibility of another element concealing the key. Despite my thorough investigation, I couldn't locate any such component. As a last resort, I decided to try the name of the ransomware gang, "shinyscorpion," and to my delight, it turned out to be the correct key!
FLAG: {Start the ransomware attack on Monday}

---------------------------------------------------------------------------------------------------------------------------------------------------------

**3.**

![Screenshot 2023-07-12 180543](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/e0615219-77df-49f6-9b01-bc35efc9c3e1)

Let me start off by saying the title of this challenge turned out to be quite deceptive! It presented a seemingly harmless .txt file containing the renowned poem "Spellbound" by Emily Brontë.
Considering the surplus of blank spaces following the sentences, I delved into the realm of whitespace steganography, conducting thorough research on the topic. During my exploration, I stumbled upon stegsnow, a widely recognized tool that employs the technique of appending whitespace to hide ASCII text within a file. Given the snowy connotation of the title, it seemed obvious to give this tool a try. However, I ende up in a rabbit hole... Later I realized all I had to do was count the whitespaces and created a simple puthon script that automatically counts it for me.

After executing the script, the output consisted of decimal numbers. Recognizing their potential significance, I proceeded to convert them to ASCII characters. Through this conversion process, I discovered the flag hidden within the text!
FLAG: {QU1X0T1CALLY}

![Screenshot 2023-07-12 184027](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/e4ffc565-a0db-40db-8298-defbc7f8b0c7)
![Screenshot 2023-07-12 185912](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/d6b1b109-f32b-41b9-9941-4ea1eb027275)






















