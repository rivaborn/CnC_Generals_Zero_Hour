# Generals/Code/Libraries/Source/WWVegas/WWLib/rc4.h

## Purpose
Implements the RC4 stream cipher for encryption/decryption.

## Responsibilities
- Provides RC4 encryption/decryption functionality
- Manages key preparation and state
- Performs in-place encryption of data buffers

## Key Types
- RC4Class (Class): Main RC4 encryption class
- RC4Key (Struct): Internal state container for RC4 algorithm

## Key Functions
### RC4Class()
- Purpose: Default constructor for RC4Class
- Calls: None

### Prepare_Key()
- Purpose: Initializes RC4 state with a given key
- Calls: None

### RC4()
- Purpose: Performs in-place encryption/decryption of a buffer
- Calls: None

## Globals
None

## Dependencies
- None (header-only implementation)
