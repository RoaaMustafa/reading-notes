# Cryptography
## [Encryption, Decryption & Hacking](https://www.khanacademy.org/computing/computers-and-internet/xcae6f4a7ff015e7d:online-data-security/xcae6f4a7ff015e7d:data-encryption-techniques/a/encryption-decryption-and-code-cracking)

One of the earliest encryption techniques is the Caesar Cipher, invented by Julius Caesar more than two thousand years ago to communicate messages to his allies.

The Caesar Cipher is a great introduction to encryption, decryption, and code cracking, thanks to its simplicity.

The Caesar Cipher is a simple substitution cipher which replaces each original letter with a different letter in the alphabet by shifting the alphabet by a certain amount.

# Decrypting a message

According to historical records, Caesar always used a shift of 3.

As long as his message recipient knew the shift amount, it was trivial for them to decode the message.


# Cracking the cipher

Imagine that a very literate and savvy enemy intercepts one of Caesar's messages.


RZ VMZ WMDIBDIB VGG AJMXZN OJ EJDI RDOC XGZJKVOMV OJ YZAZVO OCZ ZIZHT LPZZI VO OCZ IDGZ YZGOV

That enemy does not know that Caesar always uses a shift of 3, so he must attempt to "crack" the cipher without knowing the shift.

There are three main techniques he could use: frequency analysis, known plaintext, and brute force.

## Frequency analysis

Human languages tend to use some letters more than others. For example, "E" is the most popular letter in the English language. 

We can analyze the frequency of the characters in the message and identify the most likely "E" and narrow down the possible shift amounts based on that.

## Known plaintext


Another term for the original unencrypted message is plaintext. 

If the enemy already knew some part of the plaintext, it will be easier for them to crack the rest of the encrypted version.

## Brute force

There are only 25 possible shifts (not 26 — why not?).

The enemy could take some time to try out each of them and find one that yielded a sensible message. 


They wouldn't even need to try the shifts on the entire message, just the first word or two.


# Encryption, decryption, and cracking

Encryption: scrambling the data according to a secret key (in this case, the alphabet shift).

Decryption: recovering the original data from scrambled data by using the secret key.

Code cracking: uncovering the original data without knowing the secret, by using a variety of clever techniques.

## [Ceasar Cipher](https://en.wikipedia.org/wiki/Caesar_cipher)

![Ceasar Cipher]](https://microbit-challenges.readthedocs.io/en/latest/_images/shift.png)

It is a type of substitution cipher in which each letter in the plaintext is replaced by a letter some fixed number of positions down the alphabet.

For example, with a left shift of 3, D would be replaced by A, E would become B, and so on.

The method is named after Julius Caesar, who used it in his private correspondence.



