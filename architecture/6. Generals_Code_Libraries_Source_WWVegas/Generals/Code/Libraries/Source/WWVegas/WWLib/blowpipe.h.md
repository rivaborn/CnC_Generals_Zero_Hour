# Generals/Code/Libraries/Source/WWVegas/WWLib/blowpipe.h

## Purpose
Defines the `BlowPipe` class for Blowfish encryption/decryption of data streams.

## Responsibilities
- Encrypts/decrypts data using Blowfish algorithm
- Manages encryption/decryption state via `CryptControl`
- Handles key submission for the Blowfish engine
- Provides pipe interface for streaming data

## Key Types
- **BlowPipe (Class)**: Encryption/decryption pipe using Blowfish
- **CryptControl (Enum)**: Controls encryption/decryption mode (`ENCRYPT`/`DECRYPT`)
- **BlowfishEngine * (Member)**: Pointer to Blowfish engine instance

## Key Functions
### BlowPipe(CryptControl control)
- Purpose: Constructor initializing encryption/decryption mode
- Calls: None

### Flush()
- Purpose: Flushes buffered data through Blowfish engine
- Calls: Not inferable

### Put(void const * source, int slen)
- Purpose: Processes data through Blowfish engine
- Calls: Not inferable

### Key(void const * key, int length)
- Purpose: Sets encryption/decryption key for Blowfish engine
- Calls: Not inferable

## Globals
- None

## Dependencies
- `pipe.h` (base class)
- `blowfish.h` (Blowfish engine)
- `BlowfishEngine` class (external)
