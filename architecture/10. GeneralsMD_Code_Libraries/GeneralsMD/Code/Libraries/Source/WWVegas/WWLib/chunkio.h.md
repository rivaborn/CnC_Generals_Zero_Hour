# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/chunkio.h

## Purpose
Defines classes and structures for reading/writing chunk-based file formats (e.g., W3D files) with hierarchical chunk support.

## Responsibilities
- Provides `ChunkHeader` and `MicroChunkHeader` structures for chunk metadata
- Implements `ChunkSaveClass` for writing chunked data to files
- Implements `ChunkLoadClass` for parsing chunked data from files
- Manages chunk nesting with stack-based tracking (max depth 256)
- Defines convenience macros for common chunk operations

## Key Types
- **ChunkHeader (struct)**: Stores chunk type (ID) and size, with MSB flag for sub-chunk detection
- **MicroChunkHeader (struct)**: Compact header for small data chunks (8-bit type/size)
- **ChunkSaveClass (class)**: Handles writing chunked data to files
- **ChunkLoadClass (class)**: Handles reading chunked data from files
- **MAX_STACK_DEPTH (enum)**: Constant (256) for chunk nesting limit

## Key Functions
### ChunkSaveClass::Begin_Chunk
- Purpose: Starts a new chunk with given ID
- Calls: Not inferable

### ChunkSaveClass::End_Chunk
- Purpose: Finalizes current chunk and updates size
- Calls: Not inferable

### ChunkLoadClass::Open_Chunk
- Purpose: Opens next chunk in file
- Calls: Not inferable

### ChunkLoadClass::Close_Chunk
- Purpose: Closes current chunk
- Calls: Not inferable

## Globals
- None

## Dependencies
- `always.h`, `bittype.h`, `wwfile.h`, `iostruct.h`
- Uses `FileClass`, `IOVector2Struct`, `IOVector3Struct`, `IOVector4Struct`, `IOQuaternionStruct`
