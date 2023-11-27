
<h1> MrRobot Machine</h1>

Let's start!

Beginning with an Nmap to see what's on we get a list of three services

<img src="https://github.com/Jeferson1101/TryHackMe_CTF/blob/main/MrRobot/screenshots/scan.png?raw=true">

Since a Web server is open let's see it!

When opening the browser we get an introduction of an fancy terminal

<img src="https://github.com/Jeferson1101/TryHackMe_CTF/blob/main/MrRobot/screenshots/web_server.png?raw=true">

Exploring the commands provided we can see some files in the server as it's shown:

<img src="https://github.com/Jeferson1101/TryHackMe_CTF/blob/main/MrRobot/screenshots/fsociety_file.png?raw=true">
<img src="https://github.com/Jeferson1101/TryHackMe_CTF/blob/main/MrRobot/screenshots/inform_file.png?raw=true">
<img src="https://github.com/Jeferson1101/TryHackMe_CTF/blob/main/MrRobot/screenshots/question_file.png?raw=true">
<img src="https://github.com/Jeferson1101/TryHackMe_CTF/blob/main/MrRobot/screenshots/wake_up-file.png?raw=true">
<img src="https://github.com/Jeferson1101/TryHackMe_CTF/blob/main/MrRobot/screenshots/join_file.png?raw=true">

Since it's a shell-like prompt, does it let you execute something? (of course not so easy)
<img src="https://github.com/Jeferson1101/TryHackMe_CTF/blob/main/MrRobot/screenshots/shell_commands.png?raw=true">

We found some files, so let's see it we can find more!

And there it is! Look's like we have some ground to play here...

<img src="https://github.com/Jeferson1101/TryHackMe_CTF/blob/main/MrRobot/screenshots/gobuster_common.png?raw=true">
<img src="https://github.com/Jeferson1101/TryHackMe_CTF/blob/main/MrRobot/screenshots/gobuster_common2.png?raw=true">

(at this time the machine crashed, so it's ip now is 10.10.199.249)

Inside the file robots.txt we have an interisting content:

<img src="https://github.com/Jeferson1101/TryHackMe_CTF/blob/main/MrRobot/screenshots/robots.png?raw=true">

Taking a look at the file "key-1-of-3.txt" we find the first key!! 

<img src="https://github.com/Jeferson1101/TryHackMe_CTF/blob/main/MrRobot/screenshots/1key.png?raw=true">

<hr>

In the same file we have another tip, it's the "fsocity.dic" file. It is a dictionary containing some names and passwords.

<img src="https://github.com/Jeferson1101/TryHackMe_CTF/blob/main/MrRobot/screenshots/dic.png?raw=true">

Let's try bruteforce the login page found with this dictionary

