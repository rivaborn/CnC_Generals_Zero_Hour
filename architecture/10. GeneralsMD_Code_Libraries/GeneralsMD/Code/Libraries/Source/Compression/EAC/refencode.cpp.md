# GeneralsMD/Code/Libraries/Source/Compression/EAC/refencode.cpp

## Purpose
Implements the REF (Reference) compression algorithm for encoding data.

## Responsibilities
- Compresses input data using a reference-based algorithm
- Manages hash tables and links for efficient matching
- Outputs compressed data with a simple header
- Handles both quick and thorough compression modes

## Key Types
- None

## Key Functions
### matchlen
- Purpose: Calculates the length of a match between two byte sequences
- Calls: None

### refcompress
- Purpose: Performs the core REF compression algorithm
- Calls: matchlen, galloc, gfree, memset, memcpy, qmin, qmax

### REF_encode
- Purpose: Wraps the compression with a header and calls refcompress
- Calls: gputm, refcompress

## Globals
- None

## Dependencies
- codex.h, refcodex.h
- galloc, gfree, gputm, qmin, qmax, memcpy, memset
- __REFWRITE macro guard
