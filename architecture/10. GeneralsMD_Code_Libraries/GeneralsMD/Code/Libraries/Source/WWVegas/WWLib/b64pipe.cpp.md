# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/b64pipe.cpp

## Purpose
Implements a Base64 encoding/decoding pipe for data processing.

## Responsibilities
- Encodes or decodes data in chunks using Base64
- Manages internal buffers for partial data processing
- Flushes remaining data when complete

## Key Types
- **Base64Pipe (Class)**: Base64 encoding/decoding pipe
- **ENCODE/DECODE (enum)**: Pipe operation modes

## Key Functions
### Base64Pipe::Put
- Purpose: Processes data through the Base64 pipe
- Calls: `memmove`, `Base64_Encode`, `Base64_Decode`, `Pipe::Put`

### Base64Pipe::Flush
- Purpose: Flushes remaining buffered data
- Calls: `Base64_Encode`, `Base64_Decode`, `Pipe::Put`, `Pipe::Flush`

## Globals
- **PBuffer (char[])**: Plain data buffer
- **CBuffer (char[])**: Coded data buffer
- **Counter (int)**: Tracks buffered data size

## Dependencies
- `b64pipe.h`, `base64.h`, `string.h`
- `Pipe` class, `Base64_Encode`, `Base64_Decode` functions
