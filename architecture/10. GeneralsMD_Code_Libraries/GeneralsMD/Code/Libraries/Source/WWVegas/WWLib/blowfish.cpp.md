# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/blowfish.cpp

## Purpose
Implements the Blowfish encryption algorithm for data encryption and decryption.

## Responsibilities
- Provides Blowfish encryption/decryption functionality
- Manages key submission and S-Box initialization
- Handles block processing with Feistal network rounds
- Supports endian-independent byte ordering

## Key Types
- `Int` (Class): Endian-independent 32-bit integer for byte manipulation
- `BlowfishEngine` (Class): Main encryption engine class (not shown in symbols but implied)

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
- Purpose: Processes a single 8-byte block using the Feistal network
- Calls: None (uses direct array access)

### `Sub_Key_Encrypt`
- Purpose: Encrypts a block for S-Box processing
- Calls: None (uses direct array access)

## Globals
- `P_Init` (unsigned long[]): Initial permutation table
- `S_Init` (unsigned long[4][UCHAR_MAX+1]): Initial S-Box tables

## Dependencies
- `blowfish.h`: Header file for BlowfishEngine class
- `always.h`: Likely contains common includes
- `string.h`: For `memcpy` and `memmove`
- `assert.h`: For parameter validation
