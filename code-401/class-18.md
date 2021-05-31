# Cryptography

### Caesar Cipher
The Caesar Cipher is a simple substitution cipher which replaces each original letter with a different letter in the alphabet by shifting the alphabet by a certain amount.

to "crack" the cipher without knowing the shift, there are three main techniques he could use: frequency analysis, known plaintext, and brute force.

#### Frequency analysis
Human languages tend to use some letters more than others. For example, "E" is the most popular letter in the English language. We can analyze the frequency of the characters in the message and identify the most likely "E" and narrow down the possible shift amounts based on that. 

#### Known plaintext
Another term for the original unencrypted message is plaintext. If the enemy already knew some part of the plaintext, it will be easier for them to crack the rest of the encrypted version.
For example, messages tend to start with similar beginnings.

#### Brute force
There are only 25 possible shifts (not 26 — why not?). The enemy could take some time to try out each of them and find one that yielded a sensible message. They wouldn't even need to try the shifts on the entire message, just the first word or two. 

##### the three key aspects of data encryption:

- Encryption: scrambling the data according to a secret key (in this case, the alphabet shift).
- Decryption: recovering the original data from scrambled data by using the secret key.
- Code cracking: uncovering the original data without knowing the secret, by using a variety of clever techniques.