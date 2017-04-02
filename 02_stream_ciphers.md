# Stream Ciphers

- Symmetric Ciphers can be divided into two as, Block ciphers and Stream Ciphers.
- Stream ciphers encrypts data bits individually.
- Small and fast.
- Used in GSM phone devices.

- Block ciphers always encrypt a full block of data (several bits)

- Common for internet applications.

`Yi = Esi(Xi)= Xi + Si mod2`

- Security of stream ciphers depends on key stream Si;

  - It should be random and reproducible Pr(Si = 0) = Pr(Si = 1) = 0.5 etc.
  - Synchronus SC: key stream depend only on the key.
  - Asynchronus SC: key stream also defends on the ciphertext

**Why mod2 is a good addition for stream cipher?**

- Mod2 is equiv. to XOR op.
- For a random key stream, good statistic property for ciphertext.
- Inversting XOR is a simple operation (for computer)

## Throughput (Encry-decry speed) for Stream Ciphers

Performance comparison of sym. ciphers (on Pentium 4 cpu)

- DES (56bit) => 36 mbit/sec
- 3DES (112bit) => 13 mbit/sec
- AES (128bit) => 51 mbit/sec
- RC4 (choosable) => 211 mbit/sec

## Random Number Generators (RNG)

- True RNG
- Pseudorandom NG
- Cryptographically Secure RNG

### True Random Number Generators (tRNG)

- Based on a physical random process (coin flipping, dice rolling)
- Output is not predictable or reproducible.
- Used for generation of keys.

### Pseudorandom NG (pRNG)

- Generates sequences from initial seed val.
- Output is predictable and reproducible
- Usually produced as a recursive function.

For example in ASCII C:

```
seed = S0 = 12345
Si+1 = 1103515245Si + S0 mod(2^31)
// recursive
```

> Just because it is predictable, it has bad cryptographic properties.

### Cryptographically Secure pRNG (CSpRNG)

- pRNG + Output must be unpredictable.
- There is no other application of it other than using in Cryptosystems.

## One-Time Pad (OTP)

**Unconditionally secure system:** A cryptosystem is unconditionally secure if it cannot be broken even with infinite computational resources.

- Can not be cracked, but requires a one-time use pre-shared key of same size as the message.
- Not practical, and disadvantageous. (Need 1GB long key for 1 GB message.)
- A plaintext is paired with a random secret key (OTP)

## Linear Feedback Shift Registers (LFSR)

- LFSR is a shift register whose input bit is a linear function of its previous state.
- Has a degree of storage elements m.
- Max. output length is (2^m)-1
- Single LFSR generates a predictable output, if 2m output bits of an LFSR of degree m are known, the feedback of coefficient Pi of the LFSR can be found by solding a system of linear equations.
- Because of this many stream ciphers use combinations of LFSRs

## Modern Stream Cipher - Trivium

- Consists three nonlinear LFSRs (NLFSR) of length 93, 84, 111
- XOR-sun of all three outputs of NLFSR generates key stream.

## Summary

- Stream ciphers are not that popular than block ciphers. (RC4 is the most popular of them)
- One-time Pad is a provable secure but not efficient because of key length being equal to message length.
- Careful combinations of several LFSR can be a strong cipher.
