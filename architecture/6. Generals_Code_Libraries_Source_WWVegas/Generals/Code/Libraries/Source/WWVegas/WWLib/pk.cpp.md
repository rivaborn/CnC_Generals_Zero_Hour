# Generals/Code/Libraries/Source/WWVegas/WWLib/pk.cpp

## Purpose
Implements public-key cryptography (RSA-like) for key generation, encryption, and decryption.

## Responsibilities
- Generate public/private key pairs
- Encode/decode key components (modulus, exponent)
- Encrypt/decrypt data blocks using RSA algorithm
- Validate key pairs via test encryption/decryption

## Key Types
- `PKey` (Class): Public-key cryptography handler
- `BigInt` (External): Large integer arithmetic (used for modulus/exponent)
- `Straw` (External): Random number generator interface

## Key Functions
### `PKey::Generate`
- Purpose: Generates paired public/private keys
- Calls: `Generate_Prime`, `BigInt` arithmetic ops, `Encrypt`, `Decrypt`, `memcmp`

### `PKey::Encrypt`
- Purpose: Encrypts plaintext blocks using the public key
- Calls: `BigInt::exp_b_mod_c`, `memmove`

### `PKey::Decrypt`
- Purpose: Decrypts ciphertext blocks using the private key
- Calls: `BigInt::exp_b_mod_c`, `memmove`

### `PKey::Encode_Modulus` / `Decode_Modulus`
- Purpose: Serializes/deserializes modulus component
- Calls: `BigInt::DEREncode` / `DERDecode`

### `PKey::Encode_Exponent` / `Decode_Exponent`
- Purpose: Serializes/deserializes exponent component
- Calls: `BigInt::DEREncode` / `DERDecode`

## Globals
- None

## Dependencies
- `pk.h` (header for `PKey` class)
- `rndstraw.h` (random number generator)
- `BigInt` class (large integer arithmetic)
- `Generate_Prime` (external prime generator)
- `Fast_Exponent()` (external constant provider)
