**1.**

![Screenshot 2023-07-12 203306](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/05ac703b-192f-4aad-95b8-a9c49506690c)

In this particular challenge, we are presented with a pcap file. To tackle the task, we meticulously analyzed the file, carefully identifying and categorizing the various devices depicted within. During this process, I successfully identified the Blue Yeti device, which ultimately led me to discover the flag concealed within its data.

`FLAG{(B58E)(0005)}`

![Screenshot 2023-07-12 204309](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/2f6e8e9c-24ed-4a27-974a-5280ba6b7218)

----------------------------------------------------------------------------------------------------------------------------------------------------------------

**2.**

![Screenshot 2023-07-12 221309](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/1199c940-e1b3-4fe0-a924-7e698689e957)

This challenge presented a direct question that required a brief answer. After conducting a quick google search, I promptly discovered the flag

`FLAG{USBMS}`

----------------------------------------------------------------------------------------------------------------------------------------------------------------

**3.**

![Screenshot 2023-07-12 221713](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/6f69e66c-10e5-4f23-a051-18c6b27b2c75)

To tackle this challenge, I utilized CyberChef and uploaded the pcap file. I used the "extract files" operation, which allowed me to uncover several files within the pcap. While inspecting these files, I came across an image that contained the hidden flag.

`FLAG{Not_An0ther_N3twork_Pcap}`


![Screenshot 2023-07-12 222416](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/881d5ebc-1690-4325-a5af-dd2431f6f66b)
----------------------------------------------------------------------------------------------------------------------------------------------------------------

**4.**

![Screenshot 2023-07-13 001503](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/6c532353-6252-44fb-98dc-93125cf9e23c)

To solve this challenge, I began by downloading the pcap file and filtering it based on the condition usb.data_len == 4 to locate the required packets. I then exported those specific packets for further analysis. To guide me through the remaining steps, I referred to a helpful resource, specifically https://disconnect3d.pl/2016/05/02/Google-CTF-2016-For2-writeup/.

As part of the solution, I had to create a separate script to ensure that colons were added after every two characters. This step was crucial to follow the required formatting. By combining these techniques and resources, I successfully completed the challenge.

![Screenshot 2023-07-13 002442](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/60c1bd97-ad61-4133-9b62-b1f9f1faadb6)

![Screenshot 2023-07-13 003123](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/e3223ba5-aa93-431f-b8b9-d83987234b55)

`FLAG{U_are_1_Clev3r_Cat}`

------------------------------------------------------------------------------------------------------------------------------------------------------------------
**5.**

![Screenshot 2023-07-13 003640](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/cc3062f1-484a-476b-aefb-7f82bbcdb982)

In a similar scenario as before, we were provided with a pcap file and tasked with plotting the data. However, this time our objective was to convert keystroke data into their corresponding characters.

To initiate the process, I created a filter using 'usb.src == '1.11.4' and focused on identifying the HID (Human Interface Device) data within the file. To navigate through the subsequent steps, I sought guidance from a useful resource, specifically https://github.com/bolisettynihith/USB-Keyboard-Parser.

![Screenshot 2023-07-13 004401](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/e82c1011-4624-48f7-bbcf-048dec05fbe3)

I successfully implemented a Python script I found online which that played a crucial role in solving the challenge. This script was designed to leverage a set of predetermined USB hex codes and perform an iterative process through the data stored in the keypress_data.txt file. As a result of this execution, I achieved the desired outcome, obtaining the flag.

`FLAG{I_See_You_F0und_The_Key$}`

![Screenshot 2023-07-13 005825](https://github.com/Chikao28/CTF-Capture-The-Flag-Writeups/assets/90115832/57b3bd6c-ea3b-4cbc-9cb1-1d841680db4c)






















