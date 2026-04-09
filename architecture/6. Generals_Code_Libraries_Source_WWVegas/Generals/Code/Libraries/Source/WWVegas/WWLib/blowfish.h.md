# Generals/Code/Libraries/Source/WWVegas/WWLib/blowfish.h

## Purpose
Header file defining the BlowfishEngine class for symmetric key block cipher encryption/decryption.

## Responsibilities
- Declares BlowfishEngine class for encryption/decryption
- Defines key submission and block processing methods
- Specifies constants for algorithm parameters (rounds, block size)
- Manages internal permutation and S-box tables

## Key Types
- BlowfishEngine (Class): symmetric key block cipher implementation
- MAX_KEY_LENGTH (Enum): maximum supported key length (56 bytes)
- ROUNDS (Enum): number of Feistal rounds (16)
- BYTES_PER_BLOCK (Enum): block size in bytes (8)

## Key Functions
### BlowfishEngine::Submit_Key
- Purpose: Initializes the encryption/decryption tables with a new key
- Calls: Initialize_Tables

### BlowfishEngine::Encrypt
- Purpose: Encrypts plaintext data using the current key
- Calls: Process_Block

### BlowfishEngine::Decrypt
- Purpose: Decrypts ciphertext data using the current key
- Calls: Process_Block

### BlowfishEngine::Process_Block
- Purpose: Processes a single 8-byte block of data
- Calls: Sub_Key_Encrypt

## Globals
- P_Init (unsigned long const[18]): Initial permutation table values
- S_Init (unsigned long const[4][256]): Initial S-box table values

## Dependencies
- bool.h (for bool type)
- <limits.h> (for UCHAR_MAX)
