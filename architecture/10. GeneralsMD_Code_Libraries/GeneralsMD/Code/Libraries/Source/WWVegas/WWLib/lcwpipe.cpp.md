# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/lcwpipe.cpp

## Purpose
Implements a data processing pipe for LCW (Lempel-Ziv-Welch) compression/decompression.

## Responsibilities
- Manages buffering and block processing for LCW compression/decompression
- Handles partial block accumulation and flushing
- Provides interface for feeding data through the pipe chain
- Maintains block headers for compressed data

## Key Types
- `LCWPipe` (Class): Main pipe class handling LCW compression/decompression
- `BlockHeader` (Struct): Contains compression statistics (comp/uncomp counts)

## Key Functions
### `LCWPipe::Put`
- Purpose: Processes input data through the LCW pipe (compress/decompress)
- Calls: `memmove`, `LCW_Uncomp`, `LCW_Comp`, `Pipe::Put`

### `LCWPipe::Flush`
- Purpose: Forces processing of any buffered data
- Calls: `Pipe::Put`, `Pipe::Flush`, `LCW_Comp`

### `LCWPipe::LCWPipe` (Constructor)
- Purpose: Initializes the pipe with given control mode and block size
- Calls: `new[]` for buffer allocation

### `LCWPipe::~LCWPipe` (Destructor)
- Purpose: Cleans up allocated buffers
- Calls: `delete[]` for buffer deallocation

## Globals
- None

## Dependencies
- `lcw.h`, `lcwpipe.h`, `always.h`
- `memmove`, `assert`
- `LCW_Uncomp`, `LCW_Comp` (external LCW functions)
- Inherits from `Pipe` class
