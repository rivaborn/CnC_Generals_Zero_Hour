# Generals/Code/Libraries/Source/WWVegas/WWLib/PK.H

## Purpose
Defines the `PKey` class for public-key cryptography operations, including key generation, encryption, and decryption.

## Responsibilities
- Encrypt/decrypt data using RSA-like public/private keys
- Generate cryptographic key pairs
- Encode/decode key components (modulus/exponent)
- Manage block sizes for cryptographic operations

## Key Types
- **PKey (Class)**: Public/private key cryptography handler
- **BigInt (Type)**: Used for modulus and exponent storage

## Key Functions
### `PKey(void const * exponent, void const * modulus)`
- Purpose: Initializes a key from DER-encoded exponent and modulus
- Calls: Not inferable

### `int Encrypt(void const * source, int slen, void * dest) const`
- Purpose: Encrypts data using the key
- Calls: Not inferable

### `int Decrypt(void const * source, int slen, void * dest) const`
- Purpose: Decrypts data using the key
- Calls: Not inferable

### `static void Generate(Straw & random, int bits, PKey & fastkey, PKey & slowkey)`
- Purpose: Generates a public/private key pair
- Calls: Not inferable

### `int Encode_Modulus(void * buffer) const`
- Purpose: Encodes the modulus into a buffer
- Calls: Not inferable

### `int Encode_Exponent(void * buffer) const`
- Purpose: Encodes the exponent into a buffer
- Calls: Not inferable

### `void Decode_Modulus(void * buffer)`
- Purpose: Decodes the modulus from a buffer
- Calls: Not inferable

### `void Decode_Ex
