# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/rc4.cpp

## Purpose
Implements the RC4 stream cipher for encryption and decryption.

## Responsibilities
- Initializes RC4 key state
- Prepares encryption keys of 8 or 16 bytes
- Performs RC4 encryption/decryption on byte buffers
- Provides key state management and copying

## Key Types
- RC4Class (Class): Main RC4 cipher implementation
- RC4KeyStruct (Struct): Holds RC4 state (X, Y, State[256])

## Key Functions
### RC4Class::Prepare_Key
- Purpose: Initializes RC4 key state from provided key data
- Calls: Prepare_Key_8bytes, Prepare_Key_16bytes

### RC4Class::RC4
- Purpose: Encrypts/decrypts a buffer using RC4 stream cipher
- Calls: None

### RC4Class::Prepare_Key_8bytes
- Purpose: Prepares 8-byte encryption key
- Calls: None

### RC4Class::Prepare_Key_16bytes
- Purpose: Prepares 16-byte encryption key
- Calls: None

## Globals
- RC4_Temp_Byte (unsigned char): Temporary storage for byte swapping
- RC4_Table_Init (unsigned char[256]): Initial state table for RC4

## Dependencies
- rc4.h (header)
- memory.h (memcpy, memset)
- stdio.h (printf)
