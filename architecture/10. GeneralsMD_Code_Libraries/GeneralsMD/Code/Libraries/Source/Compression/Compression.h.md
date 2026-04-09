# GeneralsMD/Code/Libraries/Source/Compression/Compression.h

## Purpose
Defines compression-related types and the CompressionManager interface for data compression/decompression in the SAGE engine.

## Responsibilities
- Declares compression types (enum)
- Provides static methods for compression/decompression operations
- Exposes utility functions for size calculations and type detection
- Defines naming conventions for compression methods

## Key Types
- CompressionType (Enum): enumerates supported compression algorithms (e.g., ZLIB1-9, REFPACK, NONE)
- CompressionManager (Class): static interface for compression operations

## Key Functions
### isDataCompressed
- Purpose: Checks if data is compressed
- Calls: Not inferable

### getCompressionType
- Purpose: Determines compression type of given data
- Calls: Not inferable

### getMaxCompressedSize
- Purpose: Calculates maximum possible compressed size for given uncompressed size and type
- Calls: Not inferable

### getUncompressedSize
- Purpose: Retrieves uncompressed size from compressed data
- Calls: Not inferable

### compressData
- Purpose: Compresses data using specified algorithm
- Calls: Not inferable

### decompressData
- Purpose: Decompresses data
- Calls: Not inferable

### getCompressionNameByType
- Purpose: Returns human-readable name for compression type
- Calls: Not inferable

### getDecompressionNameByType
- Purpose: Returns human-readable name for decompression (for perf timers)
- Calls: Not inferable

### getPreferredCompression
- Purpose: Returns engine's preferred compression method
- Calls: Not inferable

## Globals
None

## Dependencies
- BaseType.h (for Bool, Int types)
- Not infer
