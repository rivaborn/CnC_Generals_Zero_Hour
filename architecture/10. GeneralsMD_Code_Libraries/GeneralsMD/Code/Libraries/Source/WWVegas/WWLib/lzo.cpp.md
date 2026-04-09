# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/lzo.cpp

## Purpose
Implements LZO compression/decompression functionality for the game, using a shared work buffer and thread-safe access.

## Responsibilities
- Provides thread-safe LZO compression via `Compress()`
- Provides thread-safe LZO decompression via `Decompress()`
- Manages a shared work buffer for compression
- Includes buffer overrun detection in debug builds

## Key Types
- `LZOCompressor` (Class): wrapper for LZO compression/decompression operations

## Key Functions
### `LZOCompressor::Compress`
- Purpose: Compress input buffer using LZO algorithm
- Calls: `lzo1x_1_compress`, `CriticalSectionClass::LockClass`

### `LZOCompressor::Decompress`
- Purpose: Decompress input buffer using LZO algorithm
- Calls: `lzo1x_decompress`, `CriticalSectionClass::LockClass`

## Globals
- `WorkBuffer` (lzo_byte[]): shared compression work buffer
- `EOWorkBuffer` (lzo_byte*): end-of-work-buffer marker
- `mutex` (CriticalSectionClass): synchronization primitive for thread safety

## Dependencies
- `lzo.h` (LZO compression library)
- `mutex.h` (thread synchronization)
- `wwdebug.h` (debug assertions)
- `stdlib.h` (standard library)
- `lzo1x_1_compress`, `lzo1x_decompress` (external LZO functions)
