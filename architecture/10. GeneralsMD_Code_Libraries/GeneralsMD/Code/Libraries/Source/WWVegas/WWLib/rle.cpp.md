# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/rle.cpp

## Purpose
Implements RLE (Run-Length Encoding) compression and decompression for byte sequences, used for optimizing data storage and transfer.

## Responsibilities
- Compresses sequences of bytes using RLE
- Decompresses RLE-compressed byte sequences
- Handles line-specific compression/decompression with length metadata
- Manages buffer pointers and lengths during operations

## Key Types
- `RLEEngine` (Class): Core class providing RLE compression/decompression methods

## Key Functions
### `RLEEngine::Compress`
- Purpose: Compresses a sequence of bytes using RLE encoding
- Calls: `MIN`

### `RLEEngine::Line_Compress`
- Purpose: Compresses a line of data and stores the compressed length at the beginning
- Calls: `RLEEngine::Compress`

### `RLEEngine::Decompress`
- Purpose: Decompresses RLE-compressed byte sequences
- Calls: None

### `RLEEngine::Line_Decompress`
- Purpose: Decompresses line-compressed RLE data sequences
- Calls: `RLEEngine::Decompress`

## Globals
- None

## Dependencies
- `always.h`, `rle.h`, `assert.h`, `stdlib.h`
- `MIN` macro (from `always.h`)
- Standard C++ types (`unsigned char`, `int`, etc.)
