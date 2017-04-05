# AES Standard

- Most widely used symmetric cipher.
- 128bit block size block cipher
- 3 key lengths are supported: 128, 192, 256
- Efficient in both software and hardware.
- Takes 128bit blocks and gives 128bit crypted blocks, with choosable 128, 192, 256 key lengths
- 128bit (10 rounds), 192bit (12 rounds), 256bit (14 rounds)

## AES Layers
- Byte substitution
- Diffusion
  - Shift Rows
  - Mix Column
- Key Addition

## Security
- Brute-force: not possible
- Analytical: there is no analytical attack known effective than brute-force.
- Side-channel attacks: attacking the implementation of algorithm, not to the Algorithm

## Summary
- AES uses basic operations use Galois field arithmetic and provide strong diffusion and confusion.
- AES is really popular and used in IPsec or TLS.
- AES is efficient in software and hardware.
