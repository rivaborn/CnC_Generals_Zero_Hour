# Generals/Code/Libraries/Source/WWVegas/WWLib/lcwpipe.h

## Purpose
Defines the LCWPipe class for LCW compression/decompression of data streams in blocks.

## Responsibilities
- Compress/decompress data streams in configurable block sizes
- Manage staging buffers and block headers
- Handle flush operations for pending data

## Key Types
- **LCWPipe (Class)**: Wraps Pipe for LCW compression/decompression
- **CompControl (Enum)**: Controls compression/decompression mode (COMPRESS/DECOMPRESS)
- **(anonymous struct) (Struct)**: Represents block header (compressed/uncompressed sizes)

## Key Functions
### LCWPipe(CompControl, int blocksize=1024*8)
- Purpose: Constructor initializing compression/decompression mode and block size
- Calls: Not inferable

### Flush()
- Purpose: Flushes pending data in the staging buffer
- Calls: Not inferable

### Put(void const * source, int slen)
- Purpose: Adds data to the staging buffer for compression/decompression
- Calls: Not inferable

## Globals
- None

## Dependencies
- **pipe.h**: Base Pipe class
- **Not inferable**: LCW compression/decompression implementation details
