# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/b64straw.h

## Purpose
Defines a `Base64Straw` class for Base64 encoding/decoding data through a straw (stream) interface.

## Responsibilities
- Base64 encoding/decoding of data streams
- Managing internal buffers for encoding/decoding
- Controlling the direction (encode/decode) via `CodeControl` enum

## Key Types
- **Base64Straw (Class)**: Base64 encoding/decoding stream wrapper
- **CodeControl (Enum)**: Controls encoding (`ENCODE`) or decoding (`DECODE`) mode

## Key Functions
### Base64Straw(CodeControl control)
- Purpose: Constructor initializing the encoding/decoding mode
- Calls: None

### Get(void *source, int slen)
- Purpose: Processes data through the Base64 straw (encode/decode)
- Calls: Not inferable (implementation in .cpp)

## Globals
- None

## Dependencies
- `straw.h` (inherits from `Straw`)
