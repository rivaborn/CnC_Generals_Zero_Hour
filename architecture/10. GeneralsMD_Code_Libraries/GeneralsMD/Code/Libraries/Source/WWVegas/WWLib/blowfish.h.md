# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/blowfish.h

## Purpose
Header file defining the BlowfishEngine class for symmetric block cipher encryption/decryption.

## Responsibilities
- Declares BlowfishEngine class for encryption/decryption
- Defines key submission and block processing interfaces
- Specifies constants for algorithm parameters (rounds, block size)
- Provides initialization tables for the cipher

## Key Types
- BlowfishEngine (Class): Symmetric block cipher engine implementation
- (anonymous enum): Contains MAX_KEY_LENGTH constant
- (anonymous enum): Contains ROUNDS and BYTES_PER_BLOCK constants

## Key Functions
### BlowfishEngine::Submit_Key
- Purpose: Sets the encryption key for the engine
- Calls: Not inferable

### BlowfishEngine::Encrypt
- Purpose: Encrypts plaintext data using the current key
- Calls: Not inferable

### BlowfishEngine::Decrypt
- Purpose: Decrypts ciphertext data using the current key
- Calls: Not inferable

### BlowfishEngine::Sub_Key_Encrypt
- Purpose: Performs sub-key encryption on data blocks
- Calls: Not inferable

### BlowfishEngine::Process_Block
- Purpose: Processes a single block of data
- Calls: Not inferable

### BlowfishEngine::Initialize_Tables
- Purpose: Initializes the cipher's permutation and S-box tables
- Calls: Not inferable

## Globals
- P_Init (unsigned long const[ROUNDS+2]): Initial permutation table values
- S_Init (unsigned long const[4][UCHAR_MAX+1]): Initial S-box table values

## Dependencies
- bool.h: For boolean type definition
- <limits.h>: For UCHAR_MAX constant
- Not
