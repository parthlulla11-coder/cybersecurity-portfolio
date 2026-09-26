To download a file from a specific ip address what we need is a user and the password of that specific device. 

Step 1 - SSH login if you're using the remote device. 
step 2 - on your own device type in the command promt - python 3 -m http.server (It will look something like this)

<img width="831" height="130" alt="image" src="https://github.com/user-attachments/assets/994d715f-07ce-4b33-a7b7-38881759e7a3" />

Step 3 - open an terminal tab - type - wget https://you device Ip address for the download:port number that you got from the step 2/file name. Example - 

<img width="891" height="554" alt="image" src="https://github.com/user-attachments/assets/01b3a261-1b40-40e2-bc04-ec0b57bf04f7" />
<img width="884" height="365" alt="image" src="https://github.com/user-attachments/assets/3fc65f24-54f6-457a-be74-95ece94a641a" />

Note if the file is like .myfile (It's hidden you won't be seeing thins with the command ls use ls -a to show hidden file)

<img width="892" height="549" alt="image" src="https://github.com/user-attachments/assets/bfeeeef6-2c37-4f1e-b697-2d47a30564c0" />

Now with the command ls -a 

<img width="860" height="179" alt="image" src="https://github.com/user-attachments/assets/20dd8903-5e08-472d-b8a8-c907f8aa0bbf" />

Note if you downloaded multiple times the name of the file might change like file.txt (first download) file.txt.2 (second download) and so on. 



IMPORTANT NOTE! - Once you are finished press **ctrl + c** as o**nce you open it it will keep running**. so make sure to close that server. 
