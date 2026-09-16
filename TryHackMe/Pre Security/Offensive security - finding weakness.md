Offensive Security focuses on proactively testing systems by attempting to break into them, with the goal of identifying weaknesses before real attackers can exploit them. If you’ve been working through the Pre Security path, you’ve already built a solid foundation in how computers, networks, and web technologies work. In this room, you’ll take the next step and start applying that knowledge from an attacker’s perspective.

**Learning Objectives**

* Explain what offensive security is and understand why it is used to improve system security
* Recognize common terminology and methodology used in offensive security
* Practice ethical hacking techniques in a safe, permission-based environment
* Identify next steps and learning paths to continue your offensive security journey

Finding a weakness - 

**Core Offensive Security Terms** - 

* Red Teaming: A structured, authorized attack methodology that simulates a real adversary to test the effectiveness of defenses and find vulnerabilities within a defined scope
* Penetration Test: A structured security assessment where an authorized tester attempts to identify and exploit vulnerabilities within a defined scope to understand real-world risk
* Vulnerability: A weakness or flaw in a system, application, or configuration that an attacker could abuse
* Exploit: A technique or method used to take advantage of a vulnerability to achieve a specific outcome, such as accessing restricted functionality or data
* Scope: The boundaries of what is allowed to be tested during an engagement. Scope defines which systems, applications, and actions are permitted, and what is off-limits


**Scenario and Tools**

After months of working on his business idea, Mike is finally ready to launch his website. He has invested a significant amount of time and effort in developing a product that he believes users will love. However, Mike is also aware that businesses of all sizes are targeted by attackers daily. Before going live, he wants reassurance that no sensitive or unintended pages have been left publicly accessible. You’ve been asked to perform an assessment of his web application and identify any exposed areas that could pose a security risk. Your goal is to find these weaknesses before real attackers do, and help Mike launch with confidence. When you’re ready, click the View Site button above to access the web application and begin your assessment.

* Tools used - Gobuster. ()
* command line used - gobuster dir --url http://www.onlineshop.thm/ -w /usr/share/wordlists/dirbuster/directory-list.txt

command line break up - 

* gobuster -  The command-line tool used to perform the discovery of web content
* dir - Specifies the directory and file enumeration mode, which attempts to discover hidden directories and files on a web server
* --url http://www.example.com/ Sets the target website that Gobuster will scan
* -w /usr/share/wordlists/dirbuster/directory-list.txt - Specifies the wordlist Gobuster will use to guess directory and file names (**A plain text file containing one guess per line (such as folder or file names) used by brute-forcing tools like Gobuster instead of guessing names one at a time by hand.**)

Assessment - 

****<img width="943" height="831" alt="image" src="https://github.com/user-attachments/assets/e546087d-00bd-466b-8a57-797912026b49" />


We were able to find hidden web page with go buster. 
