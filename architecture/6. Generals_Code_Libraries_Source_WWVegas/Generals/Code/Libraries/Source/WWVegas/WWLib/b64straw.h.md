# Generals/Code/Libraries/Source/WWVegas/WWLib/b64straw.h

## Purpose
Defines a `Base64Straw` class for Base64 encoding/decoding data through a straw (stream) interface.

## Responsibilities
- Encodes/decodes data in Base64 format
- Manages internal buffers for encoding/decoding
- Provides a stream-based interface for processing data

## Key Types
- **Base64Straw (Class)**: Base64 encoding/decoding straw (stream) processor
- **CodeControl (Enum)**: Controls encoding (`ENCODE`) or decoding (`DECODE`) mode

## Key Functions
### Base64Straw(CodeControl control)
- Purpose: Constructor initializing the straw with encoding/decoding mode
- Calls: None

### Get(void *source, int slen)
- Purpose: Processes data through the Base64 straw (encoding/decoding)
- Calls: Not inferable (implementation in .cpp)

## Globals
- None

## Dependencies
- `straw.h` (inherits from `Straw`)
