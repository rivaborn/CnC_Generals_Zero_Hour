# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/base64.cpp

## Purpose
Implements Base64 encoding and decoding for binary data serialization.

## Responsibilities
- Encodes binary data into Base64 ASCII format
- Decodes Base64 ASCII back into binary data
- Handles padding and partial blocks during encoding/decoding
- Provides robust error handling for malformed input

## Key Types
- `PacketType` (Union): Represents a 4-character Base64 packet with 3-byte payload
- `_decoder` (Array): Lookup table for Base64 character to 6-bit value conversion
- `BAD`/`END` (Constants): Special decoder values for invalid/end markers

## Key Functions
### Base64_Encode
- Purpose: Converts binary data to Base64 ASCII format
- Calls: None (uses only local operations and lookup tables)

### Base64_Decode
- Purpose: Converts Base64 ASCII back to binary data
- Calls: None (uses only local operations and lookup tables)

## Globals
- `_pad` (const char*): Padding character "="
- `_encoder` (const char*): Base64 character set
- `_decoder` (const unsigned char[]): Decoding lookup table
- `PacketChars` (const int): Size of Base64 packet (4)

## Dependencies
- `base64.h` (header)
- `always.h` (likely for common macros)
- Uses standard C types (char, int, unsigned char)
