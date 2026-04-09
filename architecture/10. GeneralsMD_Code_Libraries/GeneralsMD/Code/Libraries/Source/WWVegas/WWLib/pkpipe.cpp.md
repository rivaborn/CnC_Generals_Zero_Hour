# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/pkpipe.cpp

## Purpose
Implements a public-key encryption/decryption pipe using Blowfish for symmetric encryption and an unspecified public-key system.

## Responsibilities
- Manages encryption/decryption pipelines
- Handles key exchange and chaining between pipes
- Processes data streams through public-key and symmetric encryption layers
- Maintains state for key acquisition and data flow

## Key Types
- `PKPipe` (Class): Public-key encryption/decryption pipe controller
- `CryptControl` (Enum): Encryption/decryption mode (ENCRYPT/DECRYPT)
- `PKey` (Class): Public-key cryptography interface (external)
- `BlowPipe` (Class): Blowfish symmetric encryption pipe (external)
- `Pipe` (Class): Base pipe class (external)
- `RandomStraw` (Class): Random number generator (external)

## Key Functions
### `PKPipe::PKPipe`
- Purpose: Constructs a PKPipe with specified control mode and random number generator
- Calls: None

### `PKPipe::Put_To`
- Purpose: Chains this pipe to another pipe for data flow
- Calls: None

### `PKPipe::Key`
- Purpose: Sets or clears the public-key for encryption/decryption
- Calls: `Flush()`

### `PKPipe::Put`
- Purpose: Processes data through the encryption/decryption pipeline
- Calls: `Pipe::Put()`, `CipherKey->Encrypt()`, `CipherKey->Decrypt()`, `BF.Key()`

### `PKPipe::Encrypted_Key_Length`
- Purpose: Returns the encrypted key length in bytes
- Calls: `CipherKey->Block_Count()`, `CipherKey->Crypt_Block_Size()`

### `PKPipe::Plain_Key_Length`
- Purpose: Returns the plaintext key length in bytes
- Calls: `CipherKey->Block_Count()`, `CipherKey->Plain_Block_Size()`

## Globals
- `Buffer` (char[2048]): Internal buffer for key processing
- `MAX_KEY_BLOCK_SIZE` (const int): Maximum key block size (2048)
- `BLOWFISH_KEY_SIZE` (const int): Blowfish key size (56)

## Dependencies
- `pkpipe.h`, `always.h`, `string.h`
- `PKey`, `BlowPipe`, `Pipe`, `RandomStraw` classes
- `CryptControl` enum values (ENCRYPT/DECRYPT)
