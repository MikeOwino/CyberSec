In addition to using cryptography to keep things secret, you can also use cryptography to make sure your data matches what you expect. This is where hashing comes in.

Unlike the methods we’ve already looked at, which are designed to both encrypt and decrypt data, hashing is different. Hashing does not encrypt data. Instead, hashing is a one-way process that takes a piece of data of any size and uses a mathematical function to represent that data with a unique hash value of a fixed size. You cannot compute the original data from its hash.

Hashing vs Encryption Diagram

Because each hash should be unique, hashing allows us to see if changes have been made to documents. For example, when you make edits to a file on Github, GitHub hashes the file to see whether you made any changes. Similarly, if you wanted to know whether a website had changed, you could download the CSS and HTML files, hash them, and then see if you get the same value when you hash them later. If the value is different the second time, something on the website changed. No matter how large or complex your file is, hashing provides a fast, reliable way to compare files and verify their authenticity.

Ideally, hash functions always generate unique values for different inputs. When they don’t it’s called a hash collision. While it’s hypothetically possible to encounter a hash collision with nearly any hashing algorithm, with modern algorithms like SHA-256, it would take so long to result in a collision that it’s functionally impossible. Earlier hashing algorithms, like MD5 and SHA-1, are more likely to result in hash collisions.

![](https://static-assets.codecademy.com/Courses/introduction-to-cybersecurity/practical-cryptography/Cybersecurity_HashingvsEncryption_v2-08.svg)

It’s easy to get the hash value of some types data. If you are on a Unix-based operating system, open your terminal and type:

echo "Hello World" | shasum -a 256

That will give you the SHA-256 hash of the string “Hello World”. Try changing the string slightly, and you’ll see that the resulting hash changes as well.

Windows does not have a built-in function to generate hashes of Strings (although you can use Get-FileHash in Powershell to hash files), but you can easily get the SHA-256 hash of a string online.

Using Hashes to Protect Data
Hashes are widely used in order to store passwords in online databases. If passwords are stored in plaintext and a database is breached, so are all of the passwords! However, if they are stored as hash values, even if someone hacks into a website’s database, only the password hashes are exposed. For example, if your password for a website is:

CodecademyIsGr8t

But that website is storing it as a SHA-256 hash, even if someone hacked into that website, all they would see is the hash value.

d04f855e71ad9d495d91e666175d593b669f45970f885a258f6dbbaab262ac8b

Remember, an attacker has no way of “decrypting” a hash value to get the original value.

Attackers can still come up with a list of common passwords, generate hashes, and find which lines in the database match those hashes. Rainbow tables, massive tables of common passwords and password-hash combinations, speed up that process even more. However, It is practically impossible for an attacker to guess and match the hash of a complex password!

Organizations can further protect hashed information by using something called a salt. A salt is a secret random string that is combined with a password prior to hashing specifically to defend against the use of rainbow tables.

Multiple Choice Question