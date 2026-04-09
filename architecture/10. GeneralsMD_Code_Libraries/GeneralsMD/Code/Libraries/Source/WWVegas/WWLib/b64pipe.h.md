# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/b64pipe.h

## Purpose
Defines a `Base64Pipe` class for Base64 encoding/decoding of data passed through a pipe.

## Responsibilities
- Encodes/decodes data using Base64 algorithm
- Manages internal buffers for encoding/decoding
- Provides `Flush` and `Put` methods for pipe operations
- Disables copy constructor and assignment operator

## Key Types
- **Base64Pipe (Class)**: Base64 encoding/decoding pipe
- **CodeControl (Enum)**: Controls encoding/decoding mode (ENCODE/DECODE)

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
- No external symbols used
