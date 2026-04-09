# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/lzostraw.cpp

## Purpose
Implements LZOStraw class for LZO compression/decompression streaming.

## Responsibilities
- Manages LZO compression/decompression buffers
- Handles block-based data processing
- Provides Get() method for fetching processed data
- Allocates/deallocates internal buffers

## Key Types
- LZOStraw (Class): LZO compression/decompression stream handler
- BlockHeader (Struct): Contains compression block metadata (CompCount, UncompCount)

## Key Functions
### LZOStraw::LZOStraw
- Purpose: Constructor initializing compression/decompression buffers
- Calls: None

### LZOStraw::~LZOStraw
- Purpose: Destructor freeing allocated buffers
- Calls: None

### LZOStraw::Get
- Purpose: Fetches and processes data through LZO compression/decompression
- Calls: Straw::Get(), lzo1x_decompress(), lzo1x_1_compress(), memmove()

## Globals
- None

## Dependencies
- lzo.h (LZO compression library)
- lzostraw.h (class definition)
- always.h, assert.h, string.h (standard headers)
