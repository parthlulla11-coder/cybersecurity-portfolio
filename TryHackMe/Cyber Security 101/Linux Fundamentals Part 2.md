What is SSH & how Does it Work?

Secure Shell or SSH simply is a protocol between devices in an encrypted form. Using cryptography, any input we send in a human-readable format is encrypted for travelling over a network -- where it is then unencrypted once it reaches the remote machine, such as in the diagram below.

* SSH allows us to remotely execute commands on another device remotely.
* Any data sent between the devices is encrypted when it is sent over a network such as the Internet

* *"touch"*	- **Create file** - 

**Creating Files and Folders (touch, mkdir)**

Creating files and folders on Linux is a simple process. First, we'll cover creating a file. The touch command takes exactly one argument -- the name we want to give the file we create. For example, we can create the file "note" by using touch note. It's worth noting that touch simply creates a blank file. You would need to use commands like echo or text editors such as nano to add content to the blank file.

<img width="858" height="166" alt="image" src="https://github.com/user-attachments/assets/f1802470-16b5-4e6c-8432-681cc7e7fd93" />

This is a similar process for making a folder, which just involves using the mkdir command and again providing the name that we want to assign to the directory. For example, creating the directory "mydirectory" using mkdir mydirectory.

<img width="866" height="169" alt="image" src="https://github.com/user-attachments/assets/49905208-7997-41ea-a036-a01ac07c21b4" />


**Removing Files and Folders (rm)**

"rm" is extraordinary out of the commands that we've covered so far. You can simply remove files by using "rm". However, you need to provide the "-R" switch alongside the name of the directory you wish to remove.

<img width="859" height="355" alt="image" src="https://github.com/user-attachments/assets/d84cbc7a-0319-4a47-953a-cc27da285eb2" />

**Copying and Moving Files and Folders (cp, mv)**

1. the name of the existing file

2. the name we wish to assign to the new file when copying

cp copies the entire contents of the existing file into the new file. In the screenshot below, we are copying "note" to "note2".

<img width="903" height="177" alt="image" src="https://github.com/user-attachments/assets/ce33e388-53f5-4ba4-8868-1646fc86d292" />

Moving a file takes two arguments, just like the cp command. However, rather than copying and/or creating a new file, mv will merge or modify the second file that we provide as an argument. Not only can you use mv to move a file to a new folder, but you can also use mv to rename a file or folder. For example, in the screenshot below, we are renaming the file "note2" to be named "note3". "note3" will now have the contents of "note2". 

<img width="855" height="177" alt="image" src="https://github.com/user-attachments/assets/8337cea4-8d1c-4d32-bb90-29d21571728b" />

**Determining File Type**

What is often misleading and often catches people out is making presumptions from files as to what their purpose or contents may be. Files usually have what's known as an extension to make this easier. For example, text files usually have an extension of ".txt". But this is not necessary.

So far, the files we have used in our examples haven't had an extension. Without knowing the context of why the file is there -- we don't really know its purpose. Enter the file command. This command takes one argument. For example, we'll use file to confirm whether or not the "note" file in our examples is indeed a text file, like so file note.

<img width="863" height="131" alt="image" src="https://github.com/user-attachments/assets/d869bb4d-1e2a-4593-887f-3cc1641324d0" />

**Permissions 101**

certain users cannot access certain files or folders. We've previously explored some commands that can be used to determine what access we have and where it leads us. 

In our previous tasks, we learned how to extend the use of commands through flags and switches. Take, for example, the ls command, which lists the contents of the current directory. When using the -l switch, we can see ten columns such as in the screenshot below. However, we're only interested in the first three columns:

<img width="853" height="163" alt="image" src="https://github.com/user-attachments/assets/2acabe26-700a-4a6a-8086-c901aecdfee8" />

A file or folder can have a couple of characteristics that determine both what actions are allowed and what user or group has the ability to perform the given action -- such as the following:

* Read
* Write
* Execute

**Briefly: The Differences Between Users & Groups**

The great thing about Linux is that permissions can be so granular, that whilst a user technically owns a file, if the permissions have been set, then a group of users can also have either the same or a different set of permissions to the exact same file without affecting the file owner itself.

Let's put this into a real-world context; the system user that runs a web server must have permissions to read and write files for an effective web application. However, companies such as web hosting companies will have to want to allow their customers to upload their own files for their website without being the webserver system user -- compromising the security of every other customer. 

**Switching Between Users**

Switching between users on a Linux install is easy work thanks to the su command. Unless you are the root user (or using root permissions through sudo), then you are required to know two things to facilitate this transition of user accounts:

* The user we wish to **switch** to
* The user's **password**

The **su** command takes a couple of switches that may be of relevance to you. For example, executing a command once you log in or specifying a specific shell to use. I encourage you to read the man page for su to find out more. However, I will cover the **-l** or **--login** switch.

Simply, by providing the **-l** switch to **su**, we start a shell that is much more similar to the actual user logging into the system - we inherit a lot more properties of the new user, i.e., environment variables and the likes.  

<img width="851" height="157" alt="image" src="https://github.com/user-attachments/assets/8ec466f6-8902-43ea-a3bb-566199dff788" />

For example, when using su to switch to "user2", our new session drops us into our previous user's home directory.  

<img width="851" height="190" alt="image" src="https://github.com/user-attachments/assets/1189c23b-2677-4bd8-839c-ba9dc1d6ddeb" />

Where now, after using -l, our new session has dropped us into the home directory of "user" automatically. 

**Understanding File Permissions in Numeric Format**

In Linux, every file and directory has a set of permissions that control who can read, write, or execute it. These permissions are often displayed in symbolic format, such as:

<img width="854" height="69" alt="image" src="https://github.com/user-attachments/assets/198a1084-8ac5-47a6-808d-45ce1e8f0dbb" />

This format is split into three groups:

Section	Applies To	Example

<img width="852" height="280" alt="image" src="https://github.com/user-attachments/assets/aeabe938-8950-49b9-a92a-9553cf0d3265" />

Each letter represents a specific permission:

r = read
w = write
x = execute

**Converting Symbolic Permissions to Numbers**

Each permission has a numeric value:

<img width="851" height="279" alt="image" src="https://github.com/user-attachments/assets/8838ff9e-ec9c-47f4-a776-ddcd53ab24d4" />

**More Common Examples**

<img width="854" height="287" alt="image" src="https://github.com/user-attachments/assets/6a791069-7ace-45fd-b0bf-4341b9880938" />

To calculate the numeric value, we **add** the values together for each group.

<img width="887" height="402" alt="image" src="https://github.com/user-attachments/assets/3a1c4803-85a2-4472-b5d0-4e433515d72f" />

<img width="873" height="115" alt="image" src="https://github.com/user-attachments/assets/365238cd-cb2a-4a1c-ada5-8487eb0b0452" />

**Why This Matters**

Understanding numeric permissions is important because:

* Many Linux commands use numeric values (e.g. chmod 755 file)
* You can quickly identify security risks
* You can control who can access sensitive files

For example:

<img width="858" height="66" alt="image" src="https://github.com/user-attachments/assets/3694f8f4-d775-4247-83d4-2cdeea9bc855" />

This means:

* Owner: full access
* Group: read + execute
* Others: no access


**Common Directories**

**/etc - **

This root directory is one of the most important root directories on your system. The etc folder (short for etcetera) is a commonplace location to store system files that are used by your operating system. 

For example, the sudoers file highlighted in the screenshot below contains a list of the users & groups that have permission to run sudo or a set of commands as the root user.

Also highlighted below are the "passwd" and "shadow" files. These two files are special for Linux as they show how your system stores the passwords for each user in encrypted formatting called sha512.

<img width="854" height="137" alt="image" src="https://github.com/user-attachments/assets/02272b8c-c096-4192-8648-6fa78d10d1c3" />

**/var**

The "/var" directory, with "var" being short for variable data,  is one of the main root folders found on a Linux install. This folder stores data that is frequently accessed or written by services or applications running on the system. For example, log files from running services and applications are written here (/var/log), or other data that is not necessarily associated with a specific user (i.e., databases and the like).

<img width="849" height="127" alt="image" src="https://github.com/user-attachments/assets/2d7e875f-587b-427b-b933-a8e3de02d607" />

**/root**

Unlike the /home directory, the /root folder is actually the home for the "root" system user. There isn't anything more to this folder other than just understanding that this is the home directory for the "root" user. But, it is worth a mention as the logical presumption is that this user would have their data in a directory such as "/home/root" by default.  

<img width="855" height="127" alt="image" src="https://github.com/user-attachments/assets/3a1f7e37-83d4-4b2b-929c-fa41aa710f9c" />

**/tmp**

This is a unique root directory found on a Linux install. Short for "temporary", the /tmp directory is volatile and is used to store data that is only needed to be accessed once or twice. Similar to the memory on your computer, once the computer is restarted, the contents of this folder are cleared out.

What's useful for us in pentesting is that any user can write to this folder by default. Meaning once we have access to a machine, it serves as a good place to store things like our enumeration scripts.

<img width="854" height="133" alt="image" src="https://github.com/user-attachments/assets/830ab495-3632-4bd5-bff6-85a13686f4e3" />





What we learned - 

* How to connect to a Linux machine remotely using SSH
* Advancing your use of commands by providing flags, switches and where you can go to learn about these for each command (man pages)
* Some more commands that you'll frequently be using to interact with the filesystem and its contents
* A brief introduction to file permissions & switching users
* A summary paragraph of the important root directories on a Ubuntu Linux install and how we may be able to use the data stored within these.














