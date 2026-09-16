**Gobuster**

Gobuster is a fast, command-line software tool written in Go used by security professionals and penetration testers to brute-force and discover hidden files, directories, subdomains, and virtual hosts on web servers

**How Gobuster Works**

WorksGobuster works by taking a predefined list of words—known as a wordlist—and systematically testing combinations against a target website or server. It sends a high volume of HTTP or DNS requests using Go's concurrency features to see which paths or names return valid, active responses (such as a 200 OK status code), revealing hidden administrative panels, backup files, or unlinked pages. You can view the official repository and source code on the GitHub Gobuster Project. [1] (https://www.geeksforgeeks.org/linux-unix/gobuster-penetration-testing-tools-in-kali-tools/), [2] (https://hackerdna.com/blog/how-to-use-gobuster), [3] (https://en.wikipedia.org/wiki/Gobuster)

Core Modes of GobusterGobuster

IT requires you to specify a mode when running a command: 

1. Directory Mode (dir): Uncovers hidden directories and files on a website (e.g., /admin, /config.bak).
2. DNS Mode (dns): Enumerates hidden subdomains under a target domain (e.g., test.example.com).
3. Virtual Host Mode (vhost): Identifies separate virtual hostnames hosted on the same target web server IP address.
4. S3 Mode (s3): Scans for open and exposed cloud storage buckets like Amazon S3.

How to use it - 

if we want to see what www.example.com web has some hidden pages you would run the following program - 

**gobuster dir --url http://www.Example.com/ -w /usr/share/wordlists/dirbuster/directory-list.txt**

Break down - 
* gobuster The command-line tool used to perform the discovery of web content
* dir Specifies the directory and file enumeration mode, which attempts to discover hidden directories and files on a web server
* --url http://www.onlineshop.thm/ Sets the target website that Gobuster will scan
* -w /usr/share/wordlists/dirbuster/directory-list.txt Specifies the wordlist Gobuster will use to guess directory and file names

