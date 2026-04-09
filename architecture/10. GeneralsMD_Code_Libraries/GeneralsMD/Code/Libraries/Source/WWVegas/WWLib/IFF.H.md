# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/IFF.H

## Purpose
Header file defining interfaces for IFF (Interchange File Format) file handling, compression/decompression, and image loading/saving in the SAGE engine.

## Responsibilities
- Declares IFF file I/O functions (open, close, read/write chunks).
- Defines compression/decompression APIs (LCW, LZW, RLE).
- Provides image loading/saving utilities (LBM format).
- Exposes low-level assembly routines for pixel packing/compression.

## Key Types
- `PicturePlaneType` (enum): Specifies image storage format (bitplane or byte-per-pixel).
- `CompressionType` (enum): Defines supported compression methods (NOCOMPRESS, LZW, HORIZONTAL, LCW).
- `CompHeaderType` (struct): Header structure for compressed data blocks.

## Key Functions
### `Open_Iff_File`
- Purpose: Opens an IFF file for reading.
- Calls: None (external file I/O).

### `Read_Iff_Chunk`
- Purpose: Reads a chunk of data from an IFF file by ID.
- Calls: None (external file I/O).

### `LCW_Compress`
- Purpose: Compresses data using Westwood's LCW algorithm.
- Calls: None (assembly routine).

### `LCW_Uncompress`
- Purpose: Decompresses LCW-compressed data.
- Calls: None (assembly routine).

## Globals
- None.

## Dependencies
- `buff.h`: Buffer management utilities.
- `<stddef.h>`: Standard definitions.
- Assembly routines (`PACK2PLN.ASM`, `LCWCOMP.ASM`, `LCWUNCMP.ASM`).
