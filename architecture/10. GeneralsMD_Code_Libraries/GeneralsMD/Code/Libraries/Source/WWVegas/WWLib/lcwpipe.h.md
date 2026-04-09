# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/lcwpipe.h

## Purpose
Defines the LCWPipe class for LCW compression/decompression of data streams in blocks.

## Responsibilities
- Compress or decompress data streams in configurable block sizes
- Manage internal buffers and block headers
- Provide Flush and Put methods for stream processing

## Key Types
- **LCWPipe (Class)**: Wraps Pipe for LCW compression/decompression
- **CompControl (Enum)**: Controls compression/decompression mode (COMPRESS/DECOMPRESS)
- **BlockHeader (struct)**: Stores compressed/uncompressed block size metadata

## Key Functions
### LCWPipe(CompControl, int blocksize)
- Purpose: Constructor initializing compression/decompression mode and block size
- Calls: None

### Flush()
- Purpose: Flushes remaining data in the buffer
- Calls: Not inferable

### Put(void const * source, int slen)
- Purpose: Processes input data through compression/decompression
- Calls: Not inferable

## Globals
- None

## Dependencies
- **Pipe.h**: Base class for stream processing
