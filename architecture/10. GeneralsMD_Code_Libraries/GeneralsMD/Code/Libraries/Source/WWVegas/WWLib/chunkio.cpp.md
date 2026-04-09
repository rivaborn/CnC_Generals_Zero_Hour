# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/chunkio.cpp

## Purpose
Implements chunked file I/O for hierarchical data serialization, supporting nested chunks and micro-chunks.

## Responsibilities
- Manages chunked file writing (ChunkSaveClass)
- Manages chunked file reading (ChunkLoadClass)
- Handles nested chunk hierarchies with depth tracking
- Supports micro-chunks for small data items
- Provides vector/quaternion serialization helpers

## Key Types
- ChunkSaveClass (Class): Handles writing chunked data to files
- ChunkLoadClass (Class): Handles reading chunked data from files
- ChunkHeader (Struct): Stores chunk metadata (type, size, flags)
- MicroChunkHeader (Struct): Stores micro-chunk metadata (8-bit type, size)

## Key Functions
### ChunkSaveClass::Begin_Chunk
- Purpose: Starts a new chunk with given ID
- Calls: File->Seek, File->Write

### ChunkSaveClass::End_Chunk
- Purpose: Finalizes current chunk and updates parent chunk size
- Calls: File->Seek, File->Write

### ChunkSaveClass::Write
- Purpose: Writes raw data to current chunk
- Calls: File->Write

### ChunkLoadClass::Open_Chunk
- Purpose: Opens next chunk in file
- Calls: File->Read

### ChunkLoadClass::Close_Chunk
- Purpose: Closes current chunk and seeks to end
- Calls: File->Seek

### ChunkLoadClass::Read
- Purpose: Reads data from current chunk
- Calls: File->Read

## Globals
None

## Dependencies
- chunkio.h (header)
- FileClass (external file I/O interface)
- IOVector2Struct, IOVector3Struct, IOVector4Struct, IOQuaternionStruct (math types)
