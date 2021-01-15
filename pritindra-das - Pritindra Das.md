# Developer - Winter of Code 2020
# Pritindra Das
### DSC IEM : Python Reverse Shell

 I am Pritindra Das, a second year Btech student at Tezpur University, Assam. 
 In order to upskill myself, i was searching for a platform to stay motivated and work on some awesome project,
 I grabbed this opportunity of applying to WOC 2020 and got selected in the organisation DSC IEM.
 The problem statement of the project - In this project, we have created a Reverse Shell for C&C in Python 
 with extended functionalities. A reverse shell is a type  of shell in which the target machine communicates 
 back to the attacking machine. The attacking machine has a listener port on which it receives the connection,
 which by using, code or command execution is achieved. In our project we have tried to go a step further and add
 a bit more functionality to our program to add more features to the standard reverse shell.
 
 This project was mentored by - Debjeet Banerjee and Deeptendu Santra
 
# Contributions


  - So for phase 1, my objective was fixing all the easy and intermediate bugs and improving the menu system. I 
  fixed the easy bugs to an extent.

- For intermediate bugs, I tried to fix the zip extra bytes bug but wasn’t able to complete it. The bug was that
  whenever some files or folders are downloaded to the server and we unzip the files we see that some extra bytes also
  get downloaded.
  
- I made a PR regarding the encryption of bytes stream. We XORed the byte stream from client to server side.
  XOR encryption is widely used in different security sectors.
  
- For the second phase, I thought of solving two or more issues on the difficult side. But I got stuck with two issues, 
  the screenshot dependency issue and the keylogger issue. Though I got to solve the scrot dependency for screenshot with
  another function. The scrot dependency was removed with another python library, PILLOW. But I couldn’t complete building
  and executing the keylogger on the client side. 


Here are some of my PRs 
[Menu loop error handled(server side) and masking of password(server side) #10](https://github.com/whokilleddb/Reverse-Shell/pull/10) 
[Intermediate(4). Added encryption to the bytes stream. #11](https://github.com/whokilleddb/Reverse-Shell/pull/11)
[Added requirements.txt file. #13](https://github.com/whokilleddb/Reverse-Shell/pull/13)
[Difficult(4). Scrot dependency for screenshot #14](https://github.com/whokilleddb/Reverse-Shell/pull/14)

# Future Scope
I hope my contribution to the reverse shell project improved it and opens up new possibilities to make more features
and benefit from it. I hope to further contribute and motivate good work. For the future, I want to look more to the project like -
- Overall better menu system.
- Keylogger and ransomware features to it.
- webcam hijacking i.e. video sreaming from the background process.
- A web api.

# Overall Experience
Overall WOC has been a great experience for me. It was an entry for me to the open source community and motivated me for further 
contributions. My mentors have been a great help and I could learn a lot from them. I got opportunities to learn more about git, 
github, encryption, shells and a lot. Though I messed up sometimes, my mentors were kind enough to teach me and let me learn. 
I express my sincere thanks to my mentors [Debjeet Banerjee](https://github.com/whokilleddb) and [Deeptendu Santra](https://github.com/Dsantra92)
for going through my PRs and helping me throughout this month.
I hope to contribute more to the project.

Hope to participate this year too !

