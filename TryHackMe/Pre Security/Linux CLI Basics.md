Learning Objectives- 

Understand what the Linux terminal is and what it's used for.
Feel comfortable interacting with the Linux environment.
Navigate through the Linux filesystem with basic commands.

Terminal - (Using Lab machine) - 

The terminal is a text-based interface for controlling a Linux system. Instead of interacting with the graphical interface, you type commands that tell the computer exactly what to do. Cyber security professionals use it because:

It's faster than clicking around
It gives more control
Many security tools only run in the terminal

<img width="1911" height="912" alt="image" src="https://github.com/user-attachments/assets/acde4f97-50f8-40d4-947c-cbd363fd282b" />

command line used - 

 Where Am I? - pwd (print working directory)  - Showes the folder that i'm currently in.

<img width="1919" height="912" alt="image" src="https://github.com/user-attachments/assets/458769c3-13e1-42e1-babc-7ab0000b34d8" />

What's Around Me? - ls - This lists the content of the current directory. 

<img width="1919" height="914" alt="image" src="https://github.com/user-attachments/assets/b00c1bd9-fad6-4616-8977-5afbebd03579" />

If we need more details, we can try: ls -l

<img width="1916" height="910" alt="image" src="https://github.com/user-attachments/assets/c29e23fb-1224-4a1a-8ad6-210c4f879b30" />

Clear - clears the whole terminal - 
<img width="1917" height="913" alt="image" src="https://github.com/user-attachments/assets/d52855b9-7ea1-4657-8537-6576ea4064f9" />
<img width="1919" height="916" alt="image" src="https://github.com/user-attachments/assets/88f650d9-f37d-4880-a057-c010df341942" />

ls -al -  it will display all the hidden files present in the directory 
<img width="1919" height="909" alt="image" src="https://github.com/user-attachments/assets/b8cfffa7-4eb1-4c8c-badb-246654287a6b" />

Let’s Move Around - cd <directory> - navigation ex - cd - documents cd downloads etc

cd .. - for going back

find <starting_point> -name <filename> - locate files within the file system (Please note that this may take a moment, as Linux will check every folder inside your home directory. If the file exists, Linux will print the full path to it. The above result shows that the command has successfully located the file and provided us with its complete path, allowing us to navigate and read the file's content.)
ex if you need to find the mission_brief.txt - (find ~ -name mission_brief.txt)
Read the File - cat ex - cat mission_brief.txt

All commands used - 

<img width="951" height="691" alt="image" src="https://github.com/user-attachments/assets/0444bec8-8c2f-43ae-a479-749f0ddbccd5" />


Who Are You Logged in As? - whoami

What System Are You On? uname -a or uname

Check Disk and Storage Info - df -h (The -h means "human readable"; it shows sizes like 2G or 500M instead of long bytes-only numbers.)

Read a System File - cd /etc then ls to view all the files inside
