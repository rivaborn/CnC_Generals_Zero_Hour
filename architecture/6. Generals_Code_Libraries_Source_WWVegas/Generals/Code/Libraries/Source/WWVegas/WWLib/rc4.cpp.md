# Generals/Code/Libraries/Source/WWVegas/WWLib/rc4.cpp

## Purpose
Implements the RC4 stream cipher for encryption and decryption.

## Responsibilities
- Initializes RC4 state
- Prepares encryption key
- Performs RC4 encryption/decryption on buffers

## Key Types
- RC4Class (Class): Main RC4 cipher implementation
- RC4Key (Struct): Holds RC4 state (State array, X, Y)

## Key Functions
### RC4Class::RC4Class()
- Purpose: Constructor initializes RC4 state to zeros
- Calls: memset

### RC4Class::Prepare_Key()
- Purpose: Sets up the encryption key using KSA algorithm
- Calls: None (uses RC4_SWAP_BYTE macro)

### RC4Class::RC4()
- Purpose: Encrypts/decrypts buffer using PRGA algorithm
- Calls: None (uses RC4_SWAP_BYTE macro)

## Globals
- RC4_Temp_Byte (unsigned char): Temporary storage for byte swapping

## Dependencies
- rc4.h (header)
- memory.h (for memset)
- RC4_SWAP_BYTE macro (defined in this file)
