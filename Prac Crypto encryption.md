## Practical Cryptography: Encryption

![Logo](https://static-assets.codecademy.com/Courses/introduction-to-cybersecurity/practical-cryptography/alphabet_circle.png)
![](https://static-assets.codecademy.com/Courses/introduction-to-cybersecurity/practical-cryptography/key_three.png)
![](https://static-assets.codecademy.com/Courses/introduction-to-cybersecurity/practical-cryptography/Cybersecurity_SymmetricalEncryption_1.svg)

![](https://static-assets.codecademy.com/Courses/introduction-to-cybersecurity/practical-cryptography/Cybersecurity_AsymmetricalEncryption_12.svg)

![]()


How do we use encryption to send and store data securely?

Cryptography is the science of hiding data and making it available again. In cryptography, hiding data is called encryption and unhiding it is called decryption. When data is securely exchanged, it is first encrypted by the sender, and then decrypted by the receiver using a special key.

One of the earliest well-known instances of cryptography was the use of coded messages between Julius Caesar and his military generals during Roman times. This is called the “Caesar cipher”. To use it first draw the alphabet in a circle like this:

An image showing the alphabet drawn in a circle.

If our key was the number “3”, we would take every letter of the message and rotate it (move it) three places to the right, so the letter “A” would become “D”. Using this method, the word “Hello” would become “Khoor”.

This image shows the letter "A" rotated three spaces to become "D".

This is actually a very simple form of encryption, and as long as the person who receives your message knows that you used “3” as the “key” to encrypt your message, they can decrypt it as well.

How Do Computers Encrypt?
The Caesar cipher above is easily readable by a human. But how do computers, that interpret everything as binary 0s and 1s, encrypt and decrypt? The answer is the XOR operation, a key component of many complex algorithms used today, such as AES, the encryption algorithm used by the US government to protect classified information.

What is XOR? XOR is an operation that compares two bits and returns True (1) if only one of the bits is 1, and returns False (0), if the bits are the same value (both 0’s or both 1’s).

XOR gives the same string back if you perform XOR on it twice. For example, if you XOR 1100 with the key 1001, it returns 0101, and if you XOR 0101 with the same key, 1001, you get 1100 again. This may seem confusing to you, a human, but this is how computers… compute!

XOR encryption takes advantage of this reflexive property, so whatever key we XOR with a binary sequence to encrypt it, we can use that same key to decrypt the sequence. XOR is the foundation of all the common encryption methods!

The following is a secret message that was XOR-encrypted with the key cybersecurity. Try to decrypt it using this XOR Decryptor!

2b-1c-1b-45-0b-1c-10-4f-55-11-06-1a-1e-11-18-16-10-1e-12-11-0a-1a-1c-1a-54-16-0d-59-10-00-11-16-0c-15-1c-1c-0e-54-0d-0b-10-11-45-01-16-06-11-10-06-49-19-1c-10-0a-03-02-17-52-45-33-07-17-1d-00-00-43-1c-1a-06-1b-07-0c-0d-12-5e-49-06-10-04-11-16-5a
Types of Encryption
There are two main types of encryption: symmetric and asymmetric.

Symmetric encryption uses the same key to both encrypt and decrypt data.
Asymmetric encryption uses two different keys to encrypt and decrypt data.
Symmetric Encryption
Both of the examples we looked at, Caesar Cipher and basic XOR encryption, used the same key to encrypt and decrypt our data.

Symmetric encryption is the fastest way to encrypt data, and the most common for sending large chunks of data, however, it has one major vulnerability: if you send someone your key, then it’s in a form that any other person can read. That means your data is vulnerable to being stolen.

An image showing the sender and recipient encrypting and decrypting with the same key.

Asymmetric Encryption
Asymmetric encryption differs from symmetric encryption in one way: Instead of one key, you have a key pair. A key pair is made up of a public key and a private key.

The public key can be given to anyone and is only used to encrypt data.
The private key is kept secret and is only used to decrypt data.
What’s the use of having two keys? Having two keys mean you are the only person who ever has access to the private key used to decrypt data, so it is impossible for someone to intercept and read your messages.

For example, if you want to receive an encrypted message from someone, you would first generate a key pair and give them the public key. Then, they would write a message and encrypt it using the public key you gave them. Finally, they would send you the message and you would decrypt it with your private key. You never share your private key with anyone, including the recipient, so it never has a chance to be stolen. Having two keys makes sure you are the only person who can decrypt and read those messages since you are the only one with the private key.

An image showing the sender using one key to encrypt the data and the recipient using a different key to decrypt the data.

If you wanted to send a message back to the original sender they would generate a key pair as well, provide you with their public key, and you would repeat the process.

Asymmetric encryption is the most secure way to transmit data; however, it is slower and more complex than symmetric encryption. Therefore, it is primarily used to exchange smaller pieces of data.

There are a wide variety of asymmetric encryption algorithms. The most common is RSA, which is based on the factoring of prime numbers, and is functionally unbreakable if a large enough key is used (although quantum computing could change this). Another asymmetric approach is Elliptical Curve Cryptography (ECC).