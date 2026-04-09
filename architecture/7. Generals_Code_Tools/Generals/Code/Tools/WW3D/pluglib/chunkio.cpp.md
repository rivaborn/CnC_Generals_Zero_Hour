# Generals/Code/Tools/WW3D/pluglib/chunkio.cpp

## Purpose
Implements chunked file I/O for the W3D engine, handling hierarchical data structures with nested chunks and micro-chunks.

## Responsibilities
- Manages chunked file writing (ChunkSaveClass)
- Manages chunked file reading (ChunkLoadClass)
- Handles nested chunk hierarchies with depth tracking
- Supports micro-chunks for small data elements
- Provides vector/quaternion serialization

## Key Types
- ChunkSaveClass (Class): Handles writing chunked data to files
- ChunkLoadClass (Class): Handles reading chunked data from files
- ChunkHeader (Struct): Stores chunk metadata (type, size, flags)
- MicroChunkHeader (Struct): Stores micro-chunk metadata (8-bit ID, size)

## Key Functions
### ChunkSaveClass::Begin_Chunk
- Purpose: Starts a new chunk in the file
- Calls: File->Seek, File->Write

### ChunkSaveClass::End_Chunk
- Purpose: Finalizes a chunk and updates parent chunk size
- Calls: File->Seek, File->Write

### ChunkLoadClass::Open_Chunk
- Purpose: Opens and reads a chunk header from file
- Calls: File->Read

### ChunkLoadClass::Read
- Purpose: Reads data from current chunk while tracking position
- Calls: File->Read

## Globals
None

## Dependencies
- chunkio.h (header)
- FileClass (external file I/O interface)
- IOVector2Struct, IOVector3Struct, IOVector4Struct, IOQuaternionStruct (math types)
