# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/lzopipe.cpp

## Purpose
Implements LZO compression/decompression pipeline for data processing in the SAGE engine.

## Responsibilities
- Manages LZO compression/decompression of data blocks
- Handles buffer accumulation and block processing
- Provides flush mechanism for partial blocks
- Integrates with pipe chain for data flow

## Key Types
- `LZOPipe` (Class): LZO compression/decompression pipeline handler
- `BlockHeader` (Struct): Contains compressed/uncompressed block size info
- `CompControl` (Enum): Controls compression/decompression mode

## Key Functions
### `LZOPipe::Put`
- Purpose: Processes data through LZO compression/decompression pipeline
- Calls: `memmove`, `lzo1x_decompress`, `lzo1x_1_compress`, `Pipe::Put`

### `LZOPipe::Flush`
- Purpose: Flushes any partially accumulated block data
- Calls: `Pipe::Put`, `Pipe::Flush`, `lzo1x_1_compress`

## Globals
- None

## Dependencies
- `lzo.h` (LZO compression library)
- `lzopipe.h` (header for this class)
- `buff.h` (buffer management)
- `Pipe` class (base pipe functionality)
