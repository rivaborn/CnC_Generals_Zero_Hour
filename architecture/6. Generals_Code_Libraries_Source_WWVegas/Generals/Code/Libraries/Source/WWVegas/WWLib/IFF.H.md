# Generals/Code/Libraries/Source/WWVegas/WWLib/IFF.H

## Purpose
Header file defining interfaces for IFF (Interchange File Format) file handling, compression/decompression, and image loading/saving.

## Responsibilities
- Declares IFF file I/O functions
- Defines compression/decompression APIs
- Provides image loading/saving interfaces
- Declares assembly-optimized compression routines

## Key Types
- PicturePlaneType (enum): specifies image format (Amiga bitplanes or MCGA byte-per-pixel)
- CompressionType (enum): defines supported compression methods (none, LZW, RLE, LCW)
- CompHeaderType (struct): header structure for compressed data blocks

## Key Functions
### Open_Iff_File
- Purpose: Opens an IFF file for reading
- Calls: Not inferable

### Read_Iff_Chunk
- Purpose: Reads a chunk from an IFF file
- Calls: Not inferable

### LCW_Compress
- Purpose: Compresses data using Westwood's LCW algorithm
- Calls: Not inferable

### LCW_Uncompress
- Purpose: Decompresses LCW-compressed data
- Calls: Not inferable

## Globals
- None

## Dependencies
- "buff.h" for Buffer/BufferClass definitions
- <stddef.h> for standard types
- Assembly functions from PACK2PLN.ASM, LCWCOMP.ASM, LCWUNCMP.ASM
