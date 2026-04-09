# Generals/Code/Libraries/Source/WWVegas/WWLib/b64pipe.h

## Purpose
Defines a `Base64Pipe` class for Base64 encoding/decoding of data passed through a pipe.

## Responsibilities
- Base64 encoding/decoding of data streams
- Managing internal buffers for encoding/decoding
- Providing `Flush` and `Put` methods for pipe operations

## Key Types
- **Base64Pipe (Class)**: Base64 encoding/decoding pipe
- **CodeControl (Enum)**: Controls encoding (`ENCODE`) or decoding (`DECODE`) mode

## Key Functions
### Base64Pipe(CodeControl control)
- Purpose: Constructor initializing encoding/decoding mode
- Calls: None

### Flush()
- Purpose: Flushes pending data
- Calls: Not inferable

### Put(void const * source, int slen)
- Purpose: Processes input data for encoding/decoding
- Calls: Not inferable

## Globals
- None

## Dependencies
- `pipe.h` (inherits from `Pipe`)
