**1.**

![Screenshot 2023-07-12 170051](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/3ddfdc6d-4aa4-4580-9412-e4e8e84e95e7)
 
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
