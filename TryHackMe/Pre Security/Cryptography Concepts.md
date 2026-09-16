**Learning Objectives**


* Explain what cryptography is and why it matters for protecting confidentiality and integrity.
* Describe the difference between plaintext and ciphertext with actual examples.
* Explain what keys and algorithms are, and why keeping keys secret is critical.
* Explain the difference between symmetric and asymmetric encryption using everyday objects, such as lockboxes and mailboxes.
* Describe how symmetric and asymmetric encryption work together to protect your web browsing.

**Understanding the Basics**

Plaintext - A message you can read normally. Like HELLO or Patient name: Alice Smith.

Ciphertext - A scrambled version that's not supposed to make sense. Like KHOOR or Sdwlhqw qdph: Dolfh Vplwk.

Key - The secret ingredient that controls how scrambling and unscrambling work. Think of it as a password that the algorithm uses.

Algorithm - The public recipe—the set of steps that explain how to use the key on the message. Everyone can know the algorithm. Security comes from keeping the key secret.

Real-world cryptography is way more sophisticated than what we'll use here. But the basic pattern stays the same:

**Encryption process: plaintext + encryption algorithm + key  → ciphertext**

**Decryption process: ciphertext + decryptiong algorithm + key   → plaintext**

**The Lockbox Analogy**

Think about a physical lockbox:

* The algorithm is how the lock works. Anyone can see you insert a key and turn it, hence it's not secret.
* The key is your specific metal key. Only people with that exact key can open your box.
* The plaintext is the letter inside the box.
* The ciphertext is that locked box travelling through the postal system.
* Nobody tries to hide how locks work to make them secure. Security comes from keeping your key private and this same principle applies to cryptography. Algorithms are usually public and tested by experts worldwide. The security comes from keeping keys secret.

**The Caesar Cipher: Algorithm Plus Key**

**How It Works** - 

Let's say the key is 3:

A shifts forward 3 spots to become D
B becomes E
C becomes F
and so on.
X becomes A (it wraps around to the start)
Y becomes B
Z becomes C
If Alice wants to encrypt HELLO with a key of 3:

H → K
E → H
L → O
L → O
O → R
So HELLO becomes KHOOR.

To decrypt KHOOR, Bob shifts each letter backwards by 3:

K → H
H → E
O → L
O → L
R → O
He gets HELLO again. Magic? Nope. Math.


**Symmetric Encryption Explained** 

The Caesar cipher is an example of symmetric encryption. This means that:

The same key encrypts (locks) and decrypts (unlocks) the message.
Both sender and receiver need a copy of that key.
The key has to stay secret from everyone else.
Some of the benefits of using symmetric encryption are:

It's fast. Symmetric algorithms can churn through huge amounts of data really quickly.
It's efficient. Perfect for encrypting files, hard drives, and network traffic where speed matters.

The Key Distribution Problem. 

we saw how symmetric encryption works. Alice and Bob use the same key for both encryption and decryption. It's fast and efficient.

However, we also hit a wall: how do they share that key safely in the first place?

If they send it in plaintext, an attacker grabs it. If they encrypt the key, they need another key, which brings us right back to the same problem.

Enter asymmetric encryption.

Two Keys Instead of One
Asymmetric encryption uses two mathematically linked keys:

A public key that anyone can know and use.
A private key that only one person keeps secret.
Here's the clever part:

If you encrypt something with someone's public key, only their private key can decrypt it.
If you encrypt something with your private key, anyone with your public key can decrypt it (this is primarily used for digital signatures, which we won't delve into here).
The two keys are connected by some serious maths, but it would take an ordinary computer hundreds or even thousands of years to recover the private key from the public key. This computational difficulty is what makes asymmetric encryption secure.

The Mailbox Analogy - 

Let us use a physical mailbox on a street corner as an example:

The mail slot at the top is the public key. Anyone walking by can drop off a letter. It's completely open and accessible.
The locked door at the front is the private key. Only the mailbox owner has the key to open it and grab the letters.
When Alice wants to send Bob a secret:

Alice finds Bob's public key (the mail slot). This isn't a secret—Bob can post it on his website or email it around.
Alice writes her message, encrypts it with Bob's public key, and sends it.
Only Bob can decrypt it because he is the only one with the private key (the key to the door).
Even if an attacker intercepts the encrypted message, they can't decrypt it without Bob's private key.


Solving the Key Distribution Problem - 

With asymmetric encryption, Alice and Bob don't need to share a secret key beforehand. A simple flow of events can be as follows:

Bob creates a public key and a private key on his computer. He keeps the private key to himself and shares the public key with the world.
Alice grabs Bob's public key (maybe from his website or a key server).
Alice encrypts her message using Bob's public key and sends it off.
Bob receives it and decrypts it using his private key.

Real-world Use: HTTPS - 

The most common everyday use of asymmetric encryption is in HTTPS—the secure protocol you use whenever you see that padlock in your browser.

Here's what happens when you visit https://google.com:

Your browser requests the website's public key.
The website sends back its public key wrapped in a certificate (more on this shortly).
Your browser and the website use asymmetric encryption to agree on a shared secret (a symmetric key) without anyone else being able to see it.
From there on, they switch to fast symmetric encryption using that shared secret for the rest of the session.

This combo is sometimes called a hybrid approach:

Asymmetric encryption solves the problem of key distribution.
Symmetric encryption handles the heavy lifting because it's way faster.

A certificate is a digital document that:

Contains someone's public key.
States who that key belongs to (like example.com).
A trusted authority digitally signs it, called a Certificate Authority (CA).

Your browser and operating system come preloaded with a list of trusted CAs. When a website hands over a certificate:

Your browser checks that a trusted CA signed it.
Your browser checks that it's still valid (not expired or revoked).
If everything looks good, your browser shows the padlock and trusts the public key.

Viewing a Certificate In Your Browser - 

You can peek at the certificate for any HTTPS site right now. These steps can guide you to view certificates:

Visit any HTTPS site (try https://www.tryhackme.com).
Click the padlock icon in the address bar.
Look for something like "Certificate", "Connection is secure", or "View certificate".
A window opens showing details like:
Issued to: The website's domain.
Issued by: The CA that signed it.
Valid from / Valid until: The certificate's expiration dates.


what we learned - 

Plaintext is what you can read. Ciphertext is scrambled gibberish.
A key is the secret that controls scrambling and unscrambling.
An algorithm is the public method for using the key.

two flavours of encryptions - 

Symmetric encryption uses a single key for both encryption and decryption. It's fast and efficient, but you need a secure way to share that key. We used the Caesar cipher to see how this works.
Asymmetric encryption uses two linked keys: a public key that anyone can use and a private key that only one person keeps. This solves the key distribution problem and powers the initial handshake for HTTPS connections.

how real systems combine both types: 

Asymmetric encryption sets up a shared key at the start.
Symmetric encryption handles the actual data because it's faster.

Cryptography is one of the most critical tools in a defender's arsenal. It protects confidentiality and integrity, and it's the backbone of almost every secure system you use online. But it's not magic. It's one layer in a much bigger security picture that includes:

Strong password practices.
Secure key storage.
User awareness and training.
Regular software updates.
Monitoring and incident response.
