# GeneralsMD/Code/Libraries/Source/Compression/CompressionManager.cpp

## Purpose
Manages data compression and decompression using various algorithms (LZH, ZLib, BTree, Huff, RefPack).

## Responsibilities
- Detect compression type from data headers
- Compress/decompress data using selected algorithm
- Calculate max compressed size and uncompressed size
- Provide compression method names for logging

## Key Types
- `CompressionType` (enum): compression algorithm identifier
- `CompressionManager` (class): static compression utility class

## Key Functions
### `getCompressionType`
- Purpose: Detect compression type from data header
- Calls: `memcmp`

### `compressData`
- Purpose: Compress data using specified algorithm
- Calls: `BTREE_encode`, `HUFF_encode`, `REF_encode`, `CompressMemory`, `z_compress2`

### `decompressData`
- Purpose: Decompress data using detected algorithm
- Calls: `BTREE_decode`, `HUFF_decode`, `REF_decode`, `DecompressMemory`, `z_uncompress`

### `getMaxCompressedSize`
- Purpose: Calculate maximum possible compressed size
- Calls: `CalcNewSize`, `ceil`

## Globals
- `DEBUG_LOG` (macro): conditional debug logging

## Dependencies
- `Compression.h`, `NoxCompress.h`, `zlib.h`, `codex.h`, `btreecodex.h`, `huffcodex.h`, `refcodex.h`
- External compression functions: `BTREE_encode/decode`, `HUFF_encode/decode`, `REF_encode/decode`, `CompressMemory/DecompressMemory`, `z_compress2/z_uncompress`
