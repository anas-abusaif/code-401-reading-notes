# Cryptography

Encryption is a means of securing digital data using one or more mathematical techniques, along with a password or "key" used to decrypt the information. The encryption process translates information using an algorithm that makes the original information unreadable.

One of the earliest encryption techniques is the Caesar Cipher, invented by Julius Caesar more than two thousand years ago to communicate messages to his allies.
The Caesar Cipher is a great introduction to encryption, decryption, and code cracking, thanks to its simplicity.

The transformation can be represented by aligning two alphabets; the cipher alphabet is the plain alphabet rotated left or right by some number of positions. For instance, here is a Caesar cipher using a left rotation of three places, equivalent to a right shift of 23 (the shift parameter is used as the key):

Plain     A B C D E F G H I J K L M N O P Q R S T U V W X Y Z

Cipher    X Y Z A B C D E F G H I J K L M N O P Q R S T U V W

## Encryption, decryption, and cracking

Thanks to this exploration of the Caesar Cipher, we now understand the three key aspects of data encryption:

Encryption: scrambling the data according to a secret key (in this case, the alphabet shift).

Decryption: recovering the original data from scrambled data by using the secret key.

Code cracking: uncovering the original data without knowing the secret, by using a variety of clever techniques.

Whenever we consider a possible encryption technique, we need to think about all those aspects: how easy is it to encrypt? how easy is it to decrypt? And most importantly, how easy is it for a nefarious individual to crack the code?

We can no longer use the Caesar Cipher to secure our data, as it is far too easy to crack, but understanding the Cipher prepares us for understanding modern encryption techniques.
