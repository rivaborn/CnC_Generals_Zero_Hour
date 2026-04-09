# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/pkpipe.h

## Purpose
Defines the PKPipe class for encrypting/decrypting data streams using public-key and symmetric-key cryptography.

## Responsibilities
- Manages hybrid encryption (public-key for key exchange, symmetric for data)
- Handles key generation and exchange via PKey
- Processes data through Blowfish after key setup
- Controls encryption/decryption mode

## Key Types
- **PKPipe (Class)**: Hybrid encryption pipe using public-key and Blowfish
- **CryptControl (Enum)**: Controls encryption/decryption mode (ENCRYPT/DECRYPT)
- **BlowfishEngine::MAX_KEY_LENGTH (Enum)**: Blowfish key size constant
- **MAX_KEY_BLOCK_SIZE (Enum)**: Maximum key block size (256 bytes)

## Key Functions
### PKPipe::Put_To
- Purpose: Outputs processed data to another pipe
- Calls: None (virtual override)

### PKPipe::Put
- Purpose: Feeds data through for encryption/decryption processing
- Calls: None (virtual override)

### PKPipe::Key
- Purpose: Submits public key for encryption/decryption
- Calls: None

## Globals
- None

## Dependencies
- `blowpipe.h` (Blowfish encryption)
- `pipe.h` (Pipe base class)
- `pk.h` (Public-key cryptography)
- `rndstraw.h` (Random number generation)
