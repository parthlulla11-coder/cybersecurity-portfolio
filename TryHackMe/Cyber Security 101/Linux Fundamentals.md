What is Linux - 

Linux is a command line operating system based on unix. There are multiple operating systems that are based on Linux.

It's fair to say that Linux is a lot more intimidating to approach than Operating System's (OSs) such as Windows. Both variants have their own advantages and disadvantages. For example, Linux is considerably much more lightweight and you'd be surprised to know that there's a good chance you've used Linux in some form or another every day! Linux powers things such as:

Websites that you visit
Car entertainment/control panels
Point of Sale (PoS) systems such as checkout tills and registers in shops
Critical infrastructures such as traffic light controllers or industrial sensors
Phones, and similar small computing devices

Command lines - 

whoami	- tells you who you are on the system
echo - output some specific text that is provided
ls	- list what's in the current folder
cd	- change directory — move into a foldergrep
cat	- show the contents of a file
pwd	- print working directory — "where am I?"
find - 	search for files by their name. For example, find -name passwords.txt
grep -	searches inside for text. For example, grep "password123" passwords.txt

We can use a set of Linux commands to help us efficiently search for and through files. Rather than scrolling through lots of text, we can have Linux do the hard work for us. 
Real systems have millions of pieces of text and many logs. find and grep are efficient ways in Cyber security to find the important piece of information that we are looking for.

**Combine commands and capture their output**

In Linux, there are a set of special characters that can combine commands together. These are called "Operators" which tell Linux how it should process both commands. From being able to combine commands to doing what's called a redirection - sending the output of commands elsewhere. Let's go over these now:

* "&"	- Runs the command, but does not wait for it to finish before you can do anything else. The command runs in the background, and is helpful for commands that might take a while to complete, or ones that you want to keep running.
* "&&"	- Runs both commands, but waits for the first command to finish first, before the next. Like a set of dominoes.
* ">"	- Used to redirect output. We can take the output of a command and send it to a file. This operator will overwrite anything that exists in the file.
* ">>"	- This redirector does the same thing, but instead of overwriting, it will just add the output to the bottom of the file.

For example, echo hey > welcome makes a file welcome containing "hey". We can use cat welcome to verify that it worked.


