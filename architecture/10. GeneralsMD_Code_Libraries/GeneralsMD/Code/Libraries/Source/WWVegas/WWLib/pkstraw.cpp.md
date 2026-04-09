# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/pkstraw.cpp

## Purpose
Implements public-key cryptography using the PKStraw class, handling encryption/decryption with Blowfish and key management.

## Responsibilities
- Manages public-key encryption/decryption via PKStraw
- Chains straw objects for data flow
- Handles key assignment and processing
- Provides key length calculations for encrypted/decrypted states

## Key Types
- **PKStraw (Class)**: Public-key cryptography straw for Blowfish key encryption/decryption
- **CryptControl (Enum)**: Controls encryption/decryption mode (ENCRYPT/DECRYPT)
- **PKey (Struct)**: Public-key cryptography key structure

## Key Functions
### PKStraw::Get
- Purpose: Fetches and processes data through the encryption/decryption pipeline
- Calls: Straw::Get, CipherKey->Decrypt, CipherKey->Encrypt, BF.Key, Straw::Get

### PKStraw::Key
- Purpose: Assigns or removes a cipher key to the stream
- Calls: None

### PKStraw::Encrypted_Key_Length
- Purpose: Returns the encrypted key block size
- Calls: CipherKey->Block_Count, CipherKey->Crypt_Block_Size

### PKStraw::Plain_Key_Length
- Purpose: Returns the plain key block size
- Calls: CipherKey->Block_Count, CipherKey->Plain_Block_Size

## Globals
- **Buffer (char[2048])**: Internal buffer for key processing
- **MAX_KEY_BLOCK_SIZE (const int)**: Maximum key block size (2048)

## Dependencies
- **blwstraw.h**: BlowStraw class for Blowfish encryption
- **pkstraw.h**: PKStraw class declaration
- **rndstraw.h**: RandomStraw for key generation
- **always.h**: Common headers
- **string.h**: Memory functions
