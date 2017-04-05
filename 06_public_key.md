# Public Key

- Public-key algorithms have capabilities that symmetric ciphers don't have, in particular "digital signature" and "key establishment" functions.
- Computationally intensive (Slower)
- The extended **Euclidean algorithm** allows us to compute modular inverses quickly, which is important for almost all public-key schemes.

## Symmetric Cryptography

- In Symmetric Cryptography, the same secret key K is used for encryption and decryption. (Alice and Bob uses the same key k.)
- Symmetric Cr. (AES, 3DES) is really strong but;

  - Distribution of key is a problem.
  - Number of keys, for a network, every user pair must have a unique key. // n.(n-1)/2 keys needed.
  - Symmetric uses can cheat each other. (Alice can claim that he din't send a message to Bob)

## Asymmetric (Public-Key) Cryptography

- Split up the key K into; Kpub (encrypts), Kpr (Decrypts)
- Alice can send crypted message with Kpub
- Bob can read crypted message with Kpr

- Key exchange is performed with asymmetric (slow) ciphers.

- Key encryption is performed with symmetric (AES, 3DES) ciphers

## Euclidean Algorithm

> gcd (r1, r2) = gcd (r1 - r2, r2)

- gcd (27, 21) = gcd (1.21 + 6, 21)
- gcd (21, 6) = gcd (3.6 + 3, 6)
- gcd (6, 3) = gcd (2.3 + 0, 3)
- gcd (3, 0) = 3

> Do recursively.

## Summary

- The extended Euclidean algorithm allows us to compute modular inverses quickly, which is important for almost all public-key schemes.
- Only three families of public-key schemes are widely used. This is considerably fewer than in the case of symmetric algorithms.
- Public-key algorithms are computationally slow.
