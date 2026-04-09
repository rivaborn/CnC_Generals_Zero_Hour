# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/rsacrypt.h

## Purpose
Implements RSA encryption/decryption using the Int class for large integer arithmetic.

## Responsibilities
- Provides RSA encryption and decryption
- Loads RSA keys from OpenSSH identity files
- Performs key setup and precomputation for optimized decryption
- Handles large integer arithmetic via template-based precision

## Key Types
- RSACrypt (Class): RSA encryption/decryption implementation
- Integer (Class): Large integer arithmetic (from wwlib)

## Key Functions
### RSACrypt::Set_Public_Keys
- Purpose: Sets the public RSA keys (n and e)
- Calls: None

### RSACrypt::Set_Keys
- Purpose: Sets both public and private RSA keys
- Calls: Decryption_Setup()

### RSACrypt::Load_SSH_Keyset
- Purpose: Loads RSA keys from an OpenSSH identity file
- Calls: Load_Bignum(), Decryption_Setup()

### RSACrypt::Encrypt
- Purpose: Encrypts plaintext using RSA public key
- Calls: Integer::exp_b_mod_c()

### RSACrypt::Decrypt
- Purpose: Decrypts ciphertext using RSA private key
- Calls: Integer::Unsigned_Divide(), Integer::exp_b_mod_c(), XMP_Prepare_Modulus(), XMP_Mod_Mult(), XMP_Mod_Mult_Clear()

### RSACrypt::Decryption_Setup
- Purpose: Precomputes values for optimized decryption
- Calls: Integer::Unsigned_Divide(), Integer::exp_b_mod_c()

### RSACrypt::Load_Bignum
- Purpose: Loads a large integer from an SSH keyset file
- Calls: Integer::Unsigned_Decode()

## Globals
None

## Dependencies
- wwlib/int.h (Int class)
- wwlib/wwfile.h (FileClass)
- XMP_Prepare_Modulus/XMP_Mod_Mult/XMP_Mod_Mult_Clear (external multiprecision math functions)
