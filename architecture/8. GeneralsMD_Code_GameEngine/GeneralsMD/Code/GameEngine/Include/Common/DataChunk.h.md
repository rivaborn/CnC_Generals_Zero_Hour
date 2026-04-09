# GeneralsMD/Code/GameEngine/Include/Common/DataChunk.h

## Purpose
Defines classes and structures for reading and writing data chunks in a structured file format.

## Responsibilities
- Provides classes for chunked file I/O (DataChunkInput/Output)
- Manages chunk versioning and table of contents
- Supports registration of custom parsers for chunk types
- Handles binary serialization of primitive types and containers

## Key Types
- **DataChunkTableOfContents (Class)**: Manages mapping between chunk names and IDs
- **DataChunkOutput (Class)**: Handles writing chunked data to output streams
- **DataChunkInput (Class)**: Handles reading chunked data from input streams
- **UserParser (Class)**: Represents user-registered parsers for specific chunk types
- **DataChunkInfo (Struct)**: Contains metadata about a data chunk
- **Mapping (Class)**: Maps chunk names to IDs in the table of contents
- **OutputChunk/InputChunk (Class)**: Internal structures for tracking chunk state

## Key Functions
### DataChunkOutput::openDataChunk
- Purpose: Begins a new data chunk with given name and version
- Calls: Not inferable (implementation in .cpp)

### DataChunkInput::registerParser
- Purpose: Registers a callback parser for specific chunk types
- Calls: Not inferable

### DataChunkInput::parse
- Purpose: Parses the chunk stream using registered parsers
- Calls: Not inferable

## Globals
- **CHUNK_HEADER_BYTES (Enum)**: Defines size of chunk file header (4 bytes)

## Dependencies
- "Common/GameMemory.h" - Memory management utilities
- "Common/Dict.h" - Dictionary data structure
- "Common/MapReaderWriterInfo.h" - Map I/O utilities
- MemoryPoolObject - Base class for memory-pooled objects
- OutputStream/ChunkInputStream - Abstract stream interfaces
