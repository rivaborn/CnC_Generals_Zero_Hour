# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/lzopipe.h

## Purpose
Header file defining the LZOPipe class for LZO compression/decompression of data streams.

## Responsibilities
- Provides LZO compression/decompression functionality
- Manages block-based compression/decompression
- Handles data buffering and flushing
- Supports both compression and decompression modes

## Key Types
- **LZOPipe (Class)**: Main class for LZO compression/decompression
- **CompControl (Enum)**: Controls compression/decompression mode (COMPRESS/DECOMPRESS)
- **BlockHeader (struct)**: Header format for compressed blocks (CompCount, UncompCount)

## Key Functions
### LZOPipe(CompControl, int blocksize=1024*8)
- Purpose: Constructor initializing compression/decompression mode and block size
- Calls: Not inferable

### ~LZOPipe(void)
- Purpose: Destructor
- Calls: Not inferable

### Flush(void)
- Purpose: Flushes remaining data
- Calls: Not inferable

### Put(void const * source, int slen)
- Purpose: Processes input data for compression/decompression
- Calls: Not inferable

## Globals
- None

## Dependencies
- **pipe.h**: Base Pipe class
- Not inferable external symbols
