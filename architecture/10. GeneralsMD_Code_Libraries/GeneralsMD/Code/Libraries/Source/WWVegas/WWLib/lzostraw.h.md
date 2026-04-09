# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/lzostraw.h

## Purpose
Defines the `LZOStraw` class for LZO compression/decompression of data streams.

## Responsibilities
- Compress or decompress data streams via LZO algorithm
- Manage internal buffers for compression/decompression
- Handle block-based processing with headers
- Prevent copying via disabled copy constructor/assignment

## Key Types
- `LZOStraw` (Class): LZO compression/decompression stream wrapper
- `CompControl` (Enum): Mode selector (COMPRESS/DECOMPRESS)
- `BlockHeader` (Struct): Stores compressed/uncompressed block sizes

## Key Functions
### `LZOStraw(CompControl control, int blocksize)`
- Purpose: Constructor initializing compression/decompression mode and block size
- Calls: None visible

### `Get(void * source, int slen)`
- Purpose: Process data through compression/decompression pipeline
- Calls: None visible (implementation in .cpp)

## Globals
- None

## Dependencies
- `straw.h` (base class)
- LZO compression library (external)
