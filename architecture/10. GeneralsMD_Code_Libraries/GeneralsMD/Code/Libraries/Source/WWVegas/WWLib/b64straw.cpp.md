# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/b64straw.cpp

## Purpose
Implements Base64Straw::Get for encoding/decoding data streams using Base64.

## Responsibilities
- Handles Base64 encoding/decoding of data streams
- Manages buffer transfers between encoded/decoded states
- Processes data in chunks until request is fulfilled or stream exhausted

## Key Types
- Base64Straw (Class): Base64 encoding/decoding wrapper for Straw streams
- Control (Enum): ENCODE/DECODE mode selector

## Key Functions
### Base64Straw::Get
- Purpose: Fetches and converts data between Base64 and raw formats
- Calls: Straw::Get, Base64_Encode, Base64_Decode, memmove

## Globals
- PBuffer (char[]): Plaintext buffer
- CBuffer (char[]): Coded buffer
- Counter (int): Bytes available in output buffer

## Dependencies
- "always.h", "b64straw.h", "base64.h", "string.h"
- Straw::Get, Base64_Encode, Base64_Decode, memmove
