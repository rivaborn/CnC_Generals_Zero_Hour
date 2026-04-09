# Generals/Code/Libraries/Source/WWVegas/WWLib/pkpipe.h

## Purpose
Defines the PKPipe class for encrypting/decrypting data streams using a symmetric key encrypted with a public key system.

## Responsibilities
- Manages encryption/decryption using Blowfish and public key cryptography
- Handles key generation and exchange
- Processes data through a pipe interface
- Controls cryptographic operations via state flags

## Key Types
- **PKPipe (Class)**: Public key pipe for encrypted data streams
- **CryptControl (Enum)**: Controls encryption/decryption mode (ENCRYPT/DECRYPT)
- **BlowfishEngine::MAX_KEY_LENGTH (Enum)**: Blowfish key size constant
- **MAX_KEY_BLOCK_SIZE (Enum)**: Maximum key block size (256 bytes)

## Key Functions
### PKPipe::Put_To
- Purpose: Writes processed data to another pipe
- Calls: None (virtual override)

### PKPipe::Put
- Purpose: Feeds data through for encryption/decryption
- Calls: None (virtual override)

### PKPipe::Key
- Purpose: Submits key for encryption/decryption
- Calls: None

### PKPipe::Encrypted_Key_Length
- Purpose: Returns length of encrypted key
- Calls: None

### PKPipe::Plain_Key_Length
- Purpose: Returns length of plain key
- Calls: None

## Globals
- None

## Dependencies
- `blowpipe.h` (Blowfish encryption)
- `pipe.h` (Pipe base class)
- `pk.h` (Public key cryptography)
- `rndstraw.h` (Random number generation)
