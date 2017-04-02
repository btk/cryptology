# Introduction to Cryptology

- **Cryptology:** Constructing and analyzing protocols to prevent third party and public from reading the data or messages.
- **Cipher:** Encryption or decryption key or steps in order to transform subject data or message.

## Chipper Types

**Symmetric cipher:** An encrypted data can be decrypted with the same cipher. Used until 1976 widely.

**Asymmetric ciphers:** Public-key cryptography was openly proposed and is used widely since 1976.

**Hybrid Schemes:** Uses both sym. and asym. ciphers. Majority of todays protocols are hybrid.

### Symmetric Ciphers

> Alternative Names for; private-key, single-key, secret-key cryptography.

Encryption and decryption are inverse operations if the same key (K) used for both operations for example let's say x is a plain text and y is the encrypted self of it;

```
e[with K](x) = y
d[with K](y) = x
d[with K](e[with K](x)) = x
```

> The problem with this kind of secure communication is reduced to transmission and storage of key K between peers.

### Cryptanalysis

The only way to assure that a chipper is safe is to try to break it and fail.

> A cryptosystem should be secure even if the attacker knows every detail of system with the exception of the secret key.

> Only use widely known ciphers do not develop your own crypto algorithm unless an experienced CA team is checking your design.

> Do not use unproven CA or protocols. (Broken CA's)

### Attacking Cryptosystems

- Classical Attacks

  - Math. Analysis
  - Brute-force Attacks

- Implementation Attack (Reverse Engineering)

### Brute-force Attacks

Treats the cipher as a black box and checks all possible keys until condition is fulfilled (finding right key K)

> 64 bit, (2^64) => Few days or less to crack 128 bit, (2^128) => Several decades to crack (without quantum computers) 256 bit, (2^256) => Resistant even if QC is existed

## Historical Ciphers

Some historical ciphers;

### Substitution Cipher

Idea: replace each plaintext letter by a fixed other letter;

a => k b => d c => w ...

> The key for this cipher will be the replace map of the letters this means we have 26_25..2_1 = 2^88 which is infeasible with todays computers.

> Letter frequency Attack: If we know which language that the crypted text is in, (English) we can check the letter frequency in that language. This will be more helpful and accurate if we have a longer crypted text.

### Shift (Ceaser) Cipher

Replaces each plaintext letter by another one, with the rule of shifting the map k positions in the alphabet.

Lets say k = 7, then;

- textToCrypt = ATTACK = 0, 19, 19, 0, 2, 10 (positions of letters in alphabet map)
- cryptedText = HAAHR = 7, 0, 0, 7, 17 (add 7 to the positions and do mod26 on the results)

> Not safe, letter frequency analysis would crack it, also 2^26 can be cracked in several days with Brute-force.

### Affine Cipher

Extention of Shift cipher, harder to crack. k = (a, b) has two parts first will be multiplied and second will be added to the letters position.

k could be: k = (2, 1), then;

## Summary

- Don't create your own crypto algorithm if you don't have a team that will be Cryptanalysis the security of it.
- Longder key lengths is harder to crack with brute force.
- Modular aritmetic (mod) is helpful for presenting old ciphers mathematically.
