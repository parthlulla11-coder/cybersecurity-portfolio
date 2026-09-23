* "whoami" - 	tells you who you are on the system

* "echo"	- output some specific text that is provided

* "ls"	- list what's in the current folder

* "ls -a" - Shows hidden file (-a with ls)

* "cd"	- change directory — move into a folder

* "--help" - This option will list the possible options that the command accepts, provide a brief description and example of how to use it. (ls --help)

* "cat"	- show the contents of a file

* "pwd"	- print working directory — "where am I?"

* "find" - 	search for files by their name. For example, find -name passwords.txt

* "grep" - 	searches inside for text. For example, grep "password123" passwords.txt

* "&" - 	Runs the command, but does not wait for it to finish before you can do anything else. The command runs in the backgorund, and is helpful for commands that might take a while to complete, or ones that you want to keep running.

* "&&" - 	Runs both commands, but waits for the first command to finish first, before the next. Like a set of dominoes.

* ">"	- Used to redirect output. We can take the output of a command and send it to a file. This operator will overwrite anything that exists in the file.

* ">>"	- This redirector does the same thing, but instead of overwriting, it will just add the output to the bottom of the file.

* "clear" - clears whole terminal. 

* "man ls" - **we can use the man command and then provide the command we want to read the documentation for. (The manual pages are a great source of information for both system commands and applications available on both a Linux machine, which is accessible on the machine itself and online(opens in new tab).)** 

* *"touch"*	- **Create file**

* *"mkdir"*	- make directory - 	Create a folder

**Creating Files and Folders (touch, mkdir)**

Creating files and folders on Linux is a simple process. First, we'll cover creating a file. The touch command takes exactly one argument -- the name we want to give the file we create. For example, we can create the file "note" by using touch note. It's worth noting that touch simply creates a blank file. You would need to use commands like echo or text editors such as nano to add content to the blank file.

<img width="858" height="166" alt="image" src="https://github.com/user-attachments/assets/f1802470-16b5-4e6c-8432-681cc7e7fd93" />

This is a similar process for making a folder, which just involves using the mkdir command and again providing the name that we want to assign to the directory. For example, creating the directory "mydirectory" using mkdir mydirectory.

<img width="866" height="169" alt="image" src="https://github.com/user-attachments/assets/49905208-7997-41ea-a036-a01ac07c21b4" />


* "cp"	- copy	- Copy a file or folder

* "mv"	- move	- Move a file or folder

* "rm"	- remove	- Remove a file or folder (Add - R to remove the folder)

* *rm -R* - removes the folder

* "file"	- file	- Determine the type of a file


