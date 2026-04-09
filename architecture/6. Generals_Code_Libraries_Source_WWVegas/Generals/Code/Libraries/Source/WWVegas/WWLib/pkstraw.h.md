# Generals/Code/Libraries/Source/WWVegas/WWLib/pkstraw.h

## Purpose
Defines the PKStraw class for public-key encryption/decryption using Blowfish and random number generation.

## Responsibilities
- Manages public-key encryption/decryption pipeline
- Handles key exchange and Blowfish key generation
- Buffers data for block processing
- Controls encryption/decryption mode

## Key Types
- **PKStraw (Class)**: Public-key encryption/decryption straw (data processing pipeline)
- **CryptControl (Enum)**: Encryption/decryption mode control
- **BlowfishEngine::MAX_KEY_LENGTH (Enum)**: Blowfish key size constant
- **MAX_KEY_BLOCK_SIZE (Enum)**: Maximum key block size (256 bytes)

## Key Functions
### PKStraw(CryptControl control, RandomStraw & rnd)
- Purpose: Constructor initializing encryption/decryption mode and random source
- Calls: None

### Get_From(Straw * straw)
- Purpose: Retrieves data from another straw for processing
- Calls: Not inferable

### Get(void * source, int slen)
- Purpose: Processes data through the encryption/decryption pipeline
- Calls: Not inferable

### Key(PKey const * key)
- Purpose: Sets the public/private key for encryption/decryption
- Calls: None

## Globals
- None

## Dependencies
- `blwstraw.h` (BlowStraw class)
- `pk.h` (PKey class)
- `rndstraw.h` (RandomStraw class)
- Inherits from `Straw` class
