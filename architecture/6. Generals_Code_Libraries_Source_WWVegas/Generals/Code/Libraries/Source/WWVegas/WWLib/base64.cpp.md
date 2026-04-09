# Generals/Code/Libraries/Source/WWVegas/WWLib/base64.cpp

## Purpose
Implements Base64 encoding and decoding for binary data serialization.

## Responsibilities
- Encodes binary data into Base64 ASCII format
- Decodes Base64 ASCII back into binary data
- Handles padding and partial blocks during encoding/decoding

## Key Types
- PacketType (Union): Combines 3-byte input and 4-byte output representations
- (anonymous structs): Byte/bit field layouts for PacketType

## Key Functions
### Base64_Encode
- Purpose: Converts binary data to Base64 ASCII
- Calls: None (uses local variables and lookup tables)

### Base64_Decode
- Purpose: Converts Base64 ASCII back to binary data
- Calls: None (uses local variables and lookup tables)

## Globals
- _pad (char const*): Padding character "="
- _encoder (char const*): Base64 character set
- _decoder (unsigned char const[]): Lookup table for decoding
- PacketChars (int): Fixed packet size (4)

## Dependencies
- "always.h", "base64.h"
- Uses standard C types (char, int, unsigned char)
