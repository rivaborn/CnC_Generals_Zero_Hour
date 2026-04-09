# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/md5.h

## Purpose
Header file for MD5 cryptographic hash function implementation.

## Responsibilities
- Defines MD5 context structure and function prototypes
- Provides macros for MD5 function naming
- Declares core MD5 functions (init, update, finalize)

## Key Types
- MD5_CTX (Class): Holds MD5 computation state (hash value, bit count, buffer)

## Key Functions
### MD5Init
- Purpose: Initializes MD5 context
- Calls: None

### MD5Update
- Purpose: Processes input data for MD5 computation
- Calls: None

### MD5Final
- Purpose: Completes MD5 computation and stores result
- Calls: None

## Globals
- MD5Init (Function pointer): MD5 initialization function
- MD5Update (Function pointer): MD5 update function
- MD5Final (Function pointer): MD5 finalization function

## Dependencies
- UINT4 (external type)
- PROTO_LIST (external macro)
