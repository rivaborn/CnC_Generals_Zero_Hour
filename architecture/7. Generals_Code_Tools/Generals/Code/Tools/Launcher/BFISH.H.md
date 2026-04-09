# Generals/Code/Tools/Launcher/BFISH.H

## Purpose
Defines the BlowfishEngine class for encryption/decryption using the Blowfish algorithm.

## Responsibilities
- Provides encryption/decryption of data blocks
- Manages key submission and initialization
- Handles Feistal network operations for cryptography

## Key Types
- BlowfishEngine (Class): Main encryption/decryption engine
- MAX_KEY_LENGTH (Enum): Maximum supported key length (56 bytes)
- BYTES_PER_BLOCK (Enum): Block size for encryption (8 bytes)
- ROUNDS (Enum): Number of Feistal rounds (16)

## Key Functions
### Submit_Key
- Purpose: Initializes the encryption engine with a new key
- Calls: Initialize_Tables

### Encrypt
- Purpose: Encrypts plaintext into ciphertext
- Calls: Process_Block

### Decrypt
- Purpose: Decrypts ciphertext into plaintext
- Calls: Process_Block

### Sub_Key_Encrypt
- Purpose: Performs sub-key encryption for Feistal network
- Calls: None

### Process_Block
- Purpose: Processes a single block of data
- Calls: None

### Initialize_Tables
- Purpose: Initializes permutation and S-box tables
- Calls: None

## Globals
- P_Init (unsigned long const[18]): Initial permutation table values
- S_Init (unsigned long const[4][256]): Initial S-box table values

## Dependencies
- `<limits.h>` for UCHAR_MAX
- Uses unsigned long for internal operations
