# Generals/Code/GameEngine/Source/Common/System/DataChunk.cpp

## Purpose
This file implements a data chunk save/load system for Command & Conquer Generals, handling file input/output operations, including reading and writing chunks of data with compression support.

## Responsibilities
- Manage file input streams with caching and decompression.
- Handle data chunk output to temporary files before finalizing.
- Provide functions to read/write various data types (real, int, byte arrays, strings).
- Implement a system for parsing and registering user-defined parsers for specific data chunks.

## Key Types
- **CachedFileInputStream**: Manages file input with caching and decompression.
  - `m_buffer`: Stores the file content in memory.
  - `m_size`: Size of the cached buffer.
  - `m_pos`: Current position in the buffer.
  
- **DataChunkOutput**: Handles writing data chunks to a temporary file.
  - `m_pOut`: Output stream where final data is written.
  - `m_tmp_file`: Temporary file for intermediate storage.
  - `m_contents`: Manages chunk metadata.

- **DataChunkInput**: Manages reading and parsing data chunks from an input stream.
  - `m_file`: Input stream for reading data.
  - `m_chunkStack`: Stack of currently open chunks.
  - `m_parserList`: List of user-defined parsers for specific chunks.

## Key Functions
### CachedFileInputStream::open
- Purpose: Opens a file, caches its content, and decompresses it if necessary.
- Calls:
  - `TheFileSystem->openFile`
  - `CompressionManager::isDataCompressed`
  - `CompressionManager::getUncompressedSize`
  - `CompressionManager::decompressData`

### DataChunkOutput::openDataChunk
- Purpose: Opens a new data chunk for writing, storing its ID and version.
- Calls:
  - `m_contents.allocateID`
  - `fwrite` (to write chunk header)

### DataChunkInput::parse
- Purpose: Parses the input stream using registered parsers for specific chunks.
- Calls:
  - `openDataChunk`
  - `readInt`
  - `readAsciiString`
  - User-defined parsers

## Globals
- None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `stdlib.h`
  - `string.h`
  - `Compression.h`
  - `Common/DataChunk.h`
  - `Common/File.h`
  - `Common/FileSystem.h`
