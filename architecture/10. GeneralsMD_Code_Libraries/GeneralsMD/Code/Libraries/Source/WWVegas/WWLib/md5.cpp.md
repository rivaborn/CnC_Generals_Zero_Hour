# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/md5.cpp

## Purpose
Implements the MD5 message-digest algorithm for cryptographic hashing.

## Responsibilities
- Computes MD5 hash of input data
- Provides initialization, update, and finalization of MD5 context
- Handles block transformations and padding

## Key Types
- MD5_CTX (struct): MD5 computation context (state, count, buffer)
- UINT4 (typedef): 32-bit unsigned integer type

## Key Functions
### MD5Init
- Purpose: Initializes MD5 context with default values
- Calls: None

### MD5Update
- Purpose: Processes input data and updates MD5 context
- Calls: MD5_memcpy, MD5Transform

### MD5Final
- Purpose: Completes MD5 computation and produces digest
- Calls: Encode, MD5Update, MD5_memset

### MD5Transform
- Purpose: Performs core MD5 transformation on 64-byte block
- Calls: Decode, MD5_memset

### Encode/Decode
- Purpose: Converts between byte arrays and UINT4 values
- Calls: None

### MD5_memcpy/MD5_memset
- Purpose: Custom memory copy/zero functions
- Calls: None

## Globals
- PADDING (unsigned char[64]): Standard MD5 padding bytes

## Dependencies
- "global.h", "md5.h"
- UINT4, POINTER, PROTO_LIST (from includes)
