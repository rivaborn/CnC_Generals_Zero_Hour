# Generals/Code/Libraries/Source/WWVegas/WWLib/b64pipe.cpp

## Purpose
Implements a Base64 encoding/decoding pipe for data processing in the SAGE engine.

## Responsibilities
- Encodes or decodes data blocks using Base64
- Manages internal buffers for partial data processing
- Flushes remaining data when closing the pipe
- Handles data size expansion during encoding (30% growth)

## Key Types
- **Base64Pipe (Class)**: Base64 encoding/decoding pipe
- **ENCODE/DECODE (enum)**: Pipe operation modes

## Key Functions
### Base64Pipe::Put
- Purpose: Processes data through the Base64 pipe (encode/decode)
- Calls: `Pipe::Put`, `Base64_Encode`, `Base64_Decode`, `memmove`

### Base64Pipe::Flush
- Purpose: Flushes any remaining buffered data through the pipe
- Calls: `Pipe::Flush`, `Base64_Encode`, `Base64_Decode`, `Pipe::Put`

## Globals
- **PBuffer (char[256])**: Plaintext buffer
- **CBuffer (char[364])**: Coded buffer (Base64)
- **Counter (int)**: Tracks buffered data size

## Dependencies
- `b64pipe.h`, `base64.h`, `string.h`
- `Pipe` class (base class)
- `Base64_Encode`, `Base64_Decode` functions
