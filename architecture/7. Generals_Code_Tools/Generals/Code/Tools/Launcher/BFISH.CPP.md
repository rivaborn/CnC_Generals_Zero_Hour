# Generals/Code/Tools/Launcher/BFISH.CPP

## Purpose
Implements the Blowfish encryption algorithm for data encryption/decryption in the game launcher.

## Responsibilities
- Provides Blowfish encryption/decryption functionality
- Manages key submission and S-Box table generation
- Handles block processing for encryption/decryption
- Supports endian-independent byte ordering

## Key Types
- `BlowfishEngine` (Class): Main encryption engine class
- `Int` (Union): Endian-independent 32-bit integer representation
- `P_Init` (Array): Initial permutation table values
- `S_Init` (Array): Initial S-Box table values

## Key Functions
### `Submit_Key`
- Purpose: Initializes the encryption engine with a new key
- Calls: `memcpy`, `Sub_Key_Encrypt`

### `Encrypt`
- Purpose: Encrypts data using the Blowfish algorithm
- Calls: `Process_Block`, `memmove`

### `Decrypt`
- Purpose: Decrypts data using the Blowfish algorithm
- Calls: `Process_Block`, `memmove`

### `Process_Block`
- Purpose: Processes a single 8-byte block of data
- Calls: None (uses direct array access)

### `Sub_Key_Encrypt`
- Purpose: Encrypts a block for S-Box processing
- Calls: None (uses direct array access)

## Globals
- `P_Init` (Array): Initial permutation table values
- `S_Init` (Array): Initial S-Box table values

## Dependencies
- `bfish.h`: Header file for Blowfish engine
- `<string.h>`: For `memcpy` and `memmove`
- `<assert.h>`: For assertion checking
- `CHAR_BIT`: From system headers for bit manipulation
