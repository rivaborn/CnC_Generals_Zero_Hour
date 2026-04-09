# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/pk.cpp

## Purpose
Implements public-key cryptography (RSA-like) for key generation, encryption, and decryption.

## Responsibilities
- Key pair generation (public/private)
- Key encoding/decoding (DER format)
- Block-based encryption/decryption
- Key validation via test encryption/decryption

## Key Types
- **PKey (class)**: Public-key cryptography handler
- **BigInt**: Large integer arithmetic (external)
- **Straw**: Random number generator (external)

## Key Functions
### PKey::Generate
- Purpose: Generates paired public/private keys using prime numbers
- Calls: `Generate_Prime`, `Fast_Exponent`, `Encrypt`, `Decrypt`, `memcmp`

### PKey::Encrypt
- Purpose: Encrypts plaintext blocks using the public key
- Calls: `Plain_Block_Size`, `Crypt_Block_Size`, `exp_b_mod_c`, `memmove`

### PKey::Decrypt
- Purpose: Decrypts ciphertext blocks using the private key
- Calls: `Crypt_Block_Size`, `Plain_Block_Size`, `exp_b_mod_c`, `memmove`

### PKey::Encode_Modulus/Encode_Exponent
- Purpose: Encodes key components into DER format
- Calls: `DEREncode`

### PKey::Decode_Modulus/Decode_Exponent
- Purpose: Decodes DER-encoded key components
- Calls: `DERDecode`

## Globals
- **None**

## Dependencies
- `pk.h` (header)
- `rndstraw.h` (Straw class)
- `always.h`
- `string.h`
- `BigInt` class (external)
- `Generate_Prime` (external)
- `Fast_Exponent` (external)
