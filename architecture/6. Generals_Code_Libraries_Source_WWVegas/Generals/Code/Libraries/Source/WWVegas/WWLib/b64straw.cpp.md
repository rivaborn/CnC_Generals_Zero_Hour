# Generals/Code/Libraries/Source/WWVegas/WWLib/b64straw.cpp

## Purpose
Implements Base64Straw::Get for fetching and converting data to/from Base64 encoding.

## Responsibilities
- Fetches data and converts it to/from Base64 encoding
- Handles encoding/decoding based on Control flag
- Manages buffer transfers and size adjustments
- Processes data in blocks until request is fulfilled or stream exhausted

## Key Types
- Base64Straw (Class): Base64 encoding/decoding wrapper
- ENCODE/DECODE (Enum): Control flags for encoding/decoding mode

## Key Functions
### Base64Straw::Get
- Purpose: Fetches data and converts it to/from Base64 encoding
- Calls: Straw::Get, Base64_Encode, Base64_Decode, memmove

## Globals
- None

## Dependencies
- "always.h", "b64straw.h", "base64.h", "string.h"
- Straw::Get, Base64_Encode, Base64_Decode, memmove
