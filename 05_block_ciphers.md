# Block Ciphers

There are several ways of encrypting long plaintexts, e.g., an e-mail or a computer file, with a block cipher ("modes of operation")

All of the 6 modes have one goal:

- They provide confidentiality, authenticity and integrity

  - Did message come from the original sender (authenticity)
  - Was the ciphertext altered during transmission? (integrity)

## Electronic Code Book mode (ECB)

- Each Block is encrypted separately
- Block cipher operating can be parallelized
- Substitution attack is possible

## Cipher Block Chaining mode (CBC)

- The encryption of all blocks are "chained together"
- The encryption is randomized by using an initialization vector (IV)
- Substitution attack is possible

## Output Feedback mode (OFB)

- "synchronous" stream cipher from a block cipher

## Cipher Feedback mode (CFB)

- "asynchronous" stream cipher from a block cipher

## Counter mode (CTR)

- stream cipher from a block cipher, also can be paralized since the 2\. encryption canbegin before the 1\. one.

## Galois Counter Mode (GCM)

- Also computesa a message authentication code (mac)
- Checks message Authentication and message integrity

## Exhaustive Key Search

- Exhaustive key search, or brute-force search, is the basic technique of trying every possible key in turn until the correct key is identified.
- To identify the correct key it may be necessary to possess a plaintext and its corresponding ciphertext, or if the plaintext has some recognizable characteristic, ciphertext alone might suffice.
- Exhaustive key search can be mounted on any cipher and sometimes a weakness in the key schedule of the cipher can help improve the efficiency of an exhaustive key search attack.

## Increasing the Security

- Double Encryption: a plain text is encrypted 2 times with different keys of Kl and Kr
- Meet-in-the-Middle Attack: an attack for double encryption. Double Encryption is not that safe.
- Triple Encryption: Triple encryption effectively doubles the key length (3DES)
- Key Whitening: Uses 2 XOR masks before and after cipher k is ciphed. Makes block-ciphers more resistant to brute-force but not to analytical attacks.

## Summary

- Triple DES (3DES) has an effective key length of 112 bits
- Several modes can turn a block cipher into a stream cipher
- The counter mode allows parallelization of encryption and is thus suited for high speed implementations
- Double encryption with a given block cipher only marginally improves the resistance against brute-force attacks
