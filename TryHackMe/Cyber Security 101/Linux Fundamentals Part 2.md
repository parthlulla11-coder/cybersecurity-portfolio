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









