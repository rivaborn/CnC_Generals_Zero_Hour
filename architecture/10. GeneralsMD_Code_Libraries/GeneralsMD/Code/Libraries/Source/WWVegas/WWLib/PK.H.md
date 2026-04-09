# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/PK.H

## Purpose
Defines the `PKey` class for public-key cryptography operations, including key generation, encryption, and decryption.

## Responsibilities
- Encrypt/decrypt data using RSA-like public/private keys.
- Generate key pairs for cryptographic operations.
- Encode/decode key components (modulus/exponent).
- Manage block sizes for cryptographic operations.

## Key Types
- **PKey (Class)**: Public/private key cryptography handler.
- **BigInt (Type)**: Used for modulus and exponent storage (not defined here).

## Key Functions
### `PKey(void const * exponent, void const * modulus)`
- Purpose: Initializes a key from DER-encoded exponent and modulus.
- Calls: Not inferable.

### `Encrypt(void const * source, int slen, void * dest) const`
- Purpose: Encrypts data using the key.
- Calls: Not inferable.

### `Decrypt(void const * source, int slen, void * dest) const`
- Purpose: Decrypts data using the key.
- Calls: Not inferable.

### `Generate(Straw & random, int bits, PKey & fastkey, PKey & slowkey)`
- Purpose: Generates a public/private key pair.
- Calls: Not inferable.

### `Encode_Modulus(void * buffer) const`
- Purpose: Encodes the modulus into a buffer.
- Calls: Not inferable.

### `Decode_Modulus(void * buffer)`
- Purpose: Decodes the modulus from a buffer.
- Calls: Not inferable.

### `Encode_Exponent(void * buffer) const`
- Purpose: Encodes the exponent into a buffer.
- Calls: Not inferable.

### `Decode_Exponent(void * buffer)`
-
