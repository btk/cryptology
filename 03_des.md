# DES Standard

- DES is examined under block ciphers
- Encrypts block of size 64 bit.
- Considered inscure due to small key length (52 bit)
- 3DES is more secure and used widely.
- Now its replaced with AES (Advanced Encryption Standard)

## Block Cipher Primitives

- **Confusion:** An encryption operation where the relationship between key and ciphertext is "obscured". Today, a common element for achieving confusion is substitution, which is found in both AES and DES.
- **Diffusion:** An encryption operation where the influence of one plaintext symbol is "spread" over many ciphertext symbols with the goal of hiding statistical properties of the plaintext. A simple diffusion element is the bit permutation, which is frequently used within DES.

## Product Ciphers

- Most of the todays block ciphers are product ciphers.
- Consist of rounds that are applied to data repeatedly.
- Multiple transformations (permutations, substitution, modular arithmetic).
- Good diffusion.

## DES Algorithm

- Encrypts blocks of size 64 bits.
- Uses a key of size 56 bits.
- Uses same key for encryption and decryption (sym.)
- 16 rounds of identical operation
- Different subkey in each round "derived from main key"
- DES structure is a Fiestel network
- Encryption and decryption differ only in keyschedule
- L and R swapped again at the end of the cipher, i.e., after round 16 followed by a final permutation

- Main operation of DES is f-Function;

  - Expansion E
  - XOR with round key
  - S-box substitution
  - permutation

## DES Security

- Key space is too small (2^56 keys)
- S-box design is kept secret, there might be a backdoor only known by NSA
- Triple DES (3DES) consist of 3 parallel DES operations.

## Summary

- DES was dominant but not anymore because of the small bit size of 56bit.
- DES is robust agains known analitical attacks.
- Default symmetric cipher is now often AES.
