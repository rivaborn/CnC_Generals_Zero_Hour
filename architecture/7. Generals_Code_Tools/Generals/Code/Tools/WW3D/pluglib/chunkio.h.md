# Generals/Code/Tools/WW3D/pluglib/chunkio.h

## Purpose
Provides classes for reading and writing chunk-based files, similar to IFF format, with support for hierarchical chunks and micro-chunks.

## Responsibilities
- Define chunk header structures (ChunkHeader, MicroChunkHeader)
- Implement ChunkSaveClass for writing chunked data to files
- Implement ChunkLoadClass for parsing chunked data from files
- Provide macros for common chunk operations (string/micro-chunk handling)

## Key Types
- ChunkHeader (struct): Contains chunk type and size, with MSB flag for sub-chunk indication
- MicroChunkHeader (struct): Compact header for micro-chunks (single byte type/size)
- ChunkSaveClass (class): Handles writing chunked data to files
- ChunkLoadClass (class): Handles reading chunked data from files
- MAX_STACK_DEPTH (enum): Maximum recursion depth for chunk nesting (256)

## Key Functions
### ChunkSaveClass::Begin_Chunk
- Purpose: Starts a new chunk with given ID
- Calls: Not inferable

### ChunkSaveClass::End_Chunk
- Purpose: Ends current chunk and updates its size
- Calls: Not inferable

### ChunkLoadClass::Open_Chunk
- Purpose: Opens next available chunk in file
- Calls: Not inferable

### ChunkLoadClass::Close_Chunk
- Purpose: Closes current chunk and moves to parent
- Calls: Not inferable

## Globals
None

## Dependencies
- always.h, bittype.h, wwfile.h, iostruct.h
- FileClass, TCHAR, WCHAR, WWASSERT, _alloca
- IOVector2Struct, IOVector3Struct, IOVector4Struct, IOQuaternionStruct
