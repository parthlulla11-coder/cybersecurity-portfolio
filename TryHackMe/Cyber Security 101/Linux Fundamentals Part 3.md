**Nano**

It is easy to get started with Nano! To create or edit a file using nano, we simply use nano filename -- replacing "filename" with the name of the file you wish to edit.

<img width="836" height="235" alt="image" src="https://github.com/user-attachments/assets/1775c9d4-badc-4ab4-a84b-76247b125928" />

Once we press enter to execute the command, nano will launch! Where we can just begin to start entering or modifying our text. You can navigate each line using the "up" and "down" arrow keys or start a new line using the "Enter" key on your keyboard.

<img width="833" height="347" alt="image" src="https://github.com/user-attachments/assets/8e99eb2f-e2ac-428a-b2d2-fc8170456161" />

Nano has a few features that are easy to remember & covers the most general things you would want out of a text editor, including:

* Searching for text
* Copying and Pasting
* Jumping to a line number
* Finding out what line number you are on

You can use these features of nano by pressing the "Ctrl" key (which is represented as an ^ on Linux)  and a corresponding letter. For example, to exit, we would want to press "Ctrl" and "X" to exit Nano.

**General/Usefull utilities**

Downloading Files (Wget)

"wget" A powerful command-line utility for downloading files from the web. "wget" allows users to retrieve files using HTTP, HTTPS, and FTP protocols. It is particularly useful for downloading large files or multiple files at once, as it can run in the background and resume interrupted downloads. To use wget, you simply type wget <URL> in the terminal, where <URL> is the direct link to the file you want to download. For example, **wget http://example.com/file.zip** downloads the specified file to your current directory. Additionally, **wget supports various options, such as -r for recursive downloads, or -c to continue an incomplete download**. This functionality makes it a fundamental **tool** for **network operations, scripting, and automation in computing environments.**


**Transferring Files From Your Host - SCP (SSH)**

Secure copy, or SCP, is just that -- a means of securely copying files. Unlike the regular cp command, this command allows you to transfer files between two computers using the SSH protocol to provide both authentication and encryption.

Working on a model of SOURCE and DESTINATION, SCP allows you to:

* Copy files & directories from your current system to a remote system
* Copy files & directories from a remote system to your current system

Provided that we know usernames and passwords for a user on your current system and a user on the remote system. For example, let's copy an example file from our machine to a remote machine, which I have neatly laid out in the table below:

<img width="831" height="351" alt="image" src="https://github.com/user-attachments/assets/cbcb6e13-1f6c-45b8-a4b7-237b0bca5e52" />

With this information, let's craft our scp command (remembering that the format of SCP is just SOURCE and DESTINATION)

scp important.txt ubuntu@192.168.1.30:/home/ubuntu/transferred.txt

And now let's reverse this and layout the syntax for using scp to copy a file from a remote computer that we're not logged into 

<img width="812" height="370" alt="image" src="https://github.com/user-attachments/assets/008634b2-de99-4a53-845b-3288f2947651" />

The command will now look like the following: scp ubuntu@192.168.1.30:/home/ubuntu/documents.txt notes.txt 

**Serving Files From Your Host - WEB**

Ubuntu machines come pre-packaged with python3. Python helpfully provides a lightweight and easy-to-use module called "HTTPServer". This module turns your computer into a quick and easy web server that you can use to serve your own files, where they can then be downloaded by another computing using commands such as curl and wget. 

Python3's "HTTPServer" will serve the files in the directory where you run the command, but this can be changed by providing options that can be found within the manual pages. Simply, all we need to do is run python3 -m  http.server in the terminal to start the module! In the snippet below, we are serving from a directory called "webserver", which has a single named "file".

<img width="847" height="140" alt="image" src="https://github.com/user-attachments/assets/0251ee28-2788-48a4-bf18-7043fb1ea6c4" />

Now, let's use wget to download the file using the 10.48.157.140 address and the name of the file. Remember, because the python3 server is running port 8000, you will need to specify this within your wget command. For example:

<img width="838" height="114" alt="image" src="https://github.com/user-attachments/assets/43524ee2-e1ab-4b6e-aba7-11b85689d5e7" />

Note, you will need to open a new terminal to use wget and leave the one that you have started the Python3 web server in. This is because, once you start the Python3 web server, it will run in that terminal until you cancel it.

Let's take a look in the snippet below as an example:

<img width="831" height="405" alt="image" src="https://github.com/user-attachments/assets/84b6de20-c584-4b6f-be1a-167643f144f5" />

One flaw with this module is that you have no way of indexing, so you must know the exact name and location of the file that you wish to use. This is why I prefer to use Updog. What's Updog(opens in new tab)? A more advanced yet lightweight webserver. But for now, let's stick to using Python's "HTTP Server".

**Updog**

Updog is a replacement for Python's SimpleHTTPServer. It allows uploading and downloading via HTTP/S, can set ad hoc SSL certificates and use HTTP basic auth.

Installation
Install using pip:

pip install updog

Or using pipx (recommended for CLI tools):

pipx install updog

For development:

git clone https://github.com/sc0tfree/updog.git
cd updog
poetry install
poetry run updog
Usage
updog [-d DIRECTORY] [-b ADDRESS] [-p PORT] [--password PASSWORD] [--ssl | --ssl-cert CERT --ssl-key KEY] [--cors] [--hide-base-path]

Argument	Description
-d DIRECTORY, --directory DIRECTORY	Root directory [Default=.]
-b ADDRESS, --bind ADDRESS	Bind to specific address [Default=0.0.0.0]
-p PORT, --port PORT	Port to serve [Default=9090]
--password PASSWORD	Use a password to access the page. (No username)
--ssl	Enable SSL with ad-hoc certificate
--ssl-cert CERT	Path to custom SSL certificate
--ssl-key KEY	Path to custom SSL private key
--cors	Enable CORS headers
--hide-base-path	Hide full directory path (show relative paths)
--version	Show version
-h, --help	Show help
Examples
Serve from your current directory:

updog

Serve from another directory:

updog -d /another/directory

Serve from port 1234:

updog -p 1234

Password protect the page:

updog --password examplePassword123!

Please note: updog uses HTTP basic authentication. To login, you should leave the username blank and just enter the password in the password field.

Use an SSL connection (ad-hoc certificate):

updog --ssl

Use an SSL connection with custom certificates:

updog --ssl-cert /path/to/cert.pem --ssl-key /path/to/key.pem

Bind to a specific IP address:

updog -b 192.168.1.10 -p 8080

Enable CORS for web application testing:

updog --cors

Hide full directory paths (OpSec):

updog --hide-base-path

**Processes 101** - 











