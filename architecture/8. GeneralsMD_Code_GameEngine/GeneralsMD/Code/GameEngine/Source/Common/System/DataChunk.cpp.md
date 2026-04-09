# GeneralsMD/Code/GameEngine/Source/Common/System/DataChunk.cpp

## Purpose
Implements a chunked data serialization system for saving/loading game data with compression support.

## Responsibilities
- Manages chunked data streams for reading/writing
- Handles compression/decompression of data chunks
- Provides type-safe serialization for primitives, strings, and dictionaries
- Mainages chunk hierarchy and parsing registration

## Key Types
- `CachedFileInputStream` (Class): Buffered file input with compression handling
- `DataChunkOutput` (Class): Writes chunked data to output stream
- `DataChunkInput` (Class): Reads chunked data from input stream
- `OutputChunk` (Struct): Tracks chunk metadata during output
- `InputChunk` (Struct): Tracks chunk metadata during input

## Key Functions
### `CachedFileInputStream::open`
- Purpose: Opens and optionally decompresses a file into memory buffer
- Calls: `CompressionManager::isDataCompressed`, `CompressionManager::getUncompressedSize`, `CompressionManager::decompressData`

### `DataChunkOutput::openDataChunk`
- Purpose: Begins a new data chunk with given name and version
- Calls: `m_contents.allocateID`, `::fwrite`

### `DataChunkInput::parse`
- Purpose: Parses chunk stream using registered parsers
- Calls: `openDataChunk`, `closeDataChunk`, registered parser callbacks

### `DataChunkInput::readDict`
- Purpose: Deserializes a dictionary from the chunk stream
- Calls: `readInt`, `readByte`, `readReal`, `readAsciiString`, `readUnicodeString`

## Globals
- `TEMP_FILENAME` (const char*): Temporary file name for chunk output buffering

## Dependencies
- `PreRTS.h`, `Compression.h`, `DataChunk.h`, `File.h`, `FileSystem.h`
- `TheFileSystem`, `TheGlobalData`, `TheNameKeyGenerator` global instances
- `DEBUG_LOG`, `DEBUG_ASSERTCRASH`, `DEBUG_CRASH` macros
