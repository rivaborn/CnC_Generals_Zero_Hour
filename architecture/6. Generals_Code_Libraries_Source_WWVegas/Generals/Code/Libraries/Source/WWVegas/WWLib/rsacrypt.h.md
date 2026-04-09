# Generals/Code/Libraries/Source/WWVegas/WWLib/rsacrypt.h

## Purpose
Implements RSA encryption/decryption using the Int class from wwlib, supporting OpenSSH key format loading.

## Responsibilities
- RSA encryption/decryption operations
- OpenSSH identity file parsing
- Key management (public/private keys)
- Fast decryption via Chinese Remainder Theorem

## Key Types
- RSACrypt (Class): RSA cryptographic operations
- Integer (Class): Wrapper for large integer arithmetic

## Key Functions
### RSACrypt::Set_Public_Keys
- Purpose: Sets public RSA keys (n, e)
- Calls: None

### RSACrypt::Set_Keys
- Purpose: Sets public and private RSA keys
- Calls: Decryption_Setup()

### RSACrypt::Load_SSH_Keyset
- Purpose: Loads RSA keys from OpenSSH identity file
- Calls: Load_Bignum(), Decryption_Setup()

### RSACrypt::Encrypt
- Purpose: Encrypts plaintext using public key
- Calls: Integer::exp_b_mod_c()

### RSACrypt::Decrypt
- Purpose: Decrypts ciphertext using private key
- Calls: Integer::exp_b_mod_c(), XMP_* functions

### RSACrypt::Decryption_Setup
- Purpose: Precomputes values for faster decryption
- Calls: Integer::Unsigned_Divide(), Integer::exp_b_mod_c()

## Globals
None

## Dependencies
- wwlib/int.h (Int class)
- wwlib/wwfile.h (FileClass)
- XMP_* functions (external modular arithmetic)
