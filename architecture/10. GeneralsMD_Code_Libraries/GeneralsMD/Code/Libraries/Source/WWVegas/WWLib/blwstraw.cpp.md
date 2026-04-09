# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/blwstraw.cpp

## Purpose
Implements a Blowfish encryption/decryption straw (filter) for data streams.

## Responsibilities
- Encrypts/decrypts data blocks using Blowfish algorithm
- Manages partial blocks and buffer overflow
- Initializes Blowfish engine on first key submission
- Provides transparent pass-through when no key is set

## Key Types
- `BlowStraw` (Class): Blowfish encryption/decryption filter
- `BlowfishEngine` (Class): Underlying Blowfish cipher engine

## Key Functions
### `BlowStraw::Get`
- Purpose: Fetches and processes data through the Blowfish straw
- Calls: `Straw::Get`, `BF->Decrypt`, `BF->Encrypt`, `memmove`

### `BlowStraw::Key`
- Purpose: Submits a key to initialize the Blowfish engine
- Calls: `new BlowfishEngine`, `BF->Submit_Key`

## Globals
- `BF` (`BlowfishEngine*`): Pointer to the Blowfish engine instance

## Dependencies
- `blwstraw.h`, `always.h`, `string.h`, `assert.h`
- `Straw` base class
- `BlowfishEngine` class
