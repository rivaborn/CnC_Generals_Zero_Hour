# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/blwstraw.h

## Purpose
Defines the `BlowStraw` class for Blowfish encryption/decryption of data streams.

## Responsibilities
- Encrypts/decrypts data using the Blowfish algorithm
- Manages encryption/decryption state via a key
- Inherits from `Straw` for stream processing

## Key Types
- **BlowStraw (Class)**: Wrapper for Blowfish encryption/decryption of data streams
- **CryptControl (Enum)**: Controls encryption/decryption mode (`ENCRYPT`/`DECRYPT`)
- **BlowfishEngine * (Type)**: Pointer to the underlying Blowfish engine

## Key Functions
### BlowStraw(CryptControl control)
- Purpose: Constructor initializing encryption/decryption mode
- Calls: None

### ~BlowStraw()
- Purpose: Destructor cleaning up Blowfish engine
- Calls: `delete BF`

### Get(void * source, int slen)
- Purpose: Processes data through the Blowfish engine
- Calls: Not inferable (implementation in .cpp)

### Key(void const * key, int length)
- Purpose: Sets the encryption/decryption key
- Calls: Not inferable

## Globals
- None

## Dependencies
- `straw.h` (base class)
- `blowfish.h` (Blowfish engine)
- `BlowfishEngine` class (external)
