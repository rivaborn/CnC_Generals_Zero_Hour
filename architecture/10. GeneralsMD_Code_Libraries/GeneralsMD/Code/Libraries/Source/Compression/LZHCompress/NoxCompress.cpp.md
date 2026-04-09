# GeneralsMD/Code/Libraries/Source/Compression/LZHCompress/NoxCompress.cpp

## Purpose
Provides compression and decompression functionality for files and memory buffers using LZHL (LZHuff) algorithm.

## Responsibilities
- File compression/decompression
- Memory buffer compression/decompression
- Packet compression/decompression (stub implementations)
- Size calculation for compressed data

## Key Types
- None

## Key Functions
### DecompressFile
- Purpose: Decompresses a file from input to output path
- Calls: LZHLCreateDecompressor, LZHLDecompress, LZHLDestroyDecompressor

### CompressFile
- Purpose: Compresses a file from input to output path
- Calls: LZHLCreateCompressor, LZHLCompress, LZHLDestroyCompressor

### CompressPacket
- Purpose: Placeholder for packet compression (always returns true)
- Calls: None

### DecompressPacket
- Purpose: Placeholder for packet decompression (always returns true)
- Calls: None

### CalcNewSize
- Purpose: Calculates maximum compressed buffer size
- Calls: LZHLCompressorCalcMaxBuf

### DecompressMemory
- Purpose: Decompresses memory buffer
- Calls: LZHLCreateDecompressor, LZHLDecompress, LZHLDestroyDecompressor

### CompressMemory
- Purpose: Compresses memory buffer
- Calls: LZHLCreateCompressor, LZHLCompress, LZHLDestroyCompressor

## Globals
- None

## Dependencies
- `stdio.h`, `stdlib.h`
- `Lib/basetype.h`
- `Noxcompress.h`
- `CompLibHeader/lzhl.h`
- LZHL compression library functions (LZHLCreateDecompressor, LZHLDecompress, LZHLDestroyDecompressor, LZHLCreateCompressor, LZHLCompress, LZHLDestroyCompressor, LZHLCompressorCalcMaxBuf)
