# GeneralsMD/Code/GameEngine/Include/Common/MapReaderWriterInfo.h

## Purpose
Defines version constants and stream interfaces for reading/writing map data in Command & Conquer Generals.

## Responsibilities
- Declares version constants for map components (height maps, blend tiles, objects, etc.)
- Defines abstract stream classes for I/O operations
- Provides concrete implementation for file-based input streaming
- Supports chunked reading with seeking capabilities

## Key Types
- **OutputStream (Class)**: Abstract base for writing data streams
- **InputStream (Class)**: Abstract base for reading data streams
- **ChunkInputStream (Class)**: Extended input stream with seeking/tell/eof
- **CachedFileInputStream (Class)**: File-based input stream with buffering

## Key Functions
### OutputStream::write
- Purpose: Virtual method for writing data to stream
- Calls: None

### InputStream::read
- Purpose: Virtual method for reading data from stream
- Calls: None

### ChunkInputStream::read
- Purpose: Virtual method for reading with chunk support
- Calls: None

### ChunkInputStream::tell
- Purpose: Virtual method to get current position
- Calls: None

### ChunkInputStream::absoluteSeek
- Purpose: Virtual method for seeking to absolute position
- Calls: None

### ChunkInputStream::eof
- Purpose: Virtual method to check end-of-file
- Calls: None

### CachedFileInputStream::open
- Purpose: Opens file and loads into memory buffer
- Calls: None

### CachedFileInputStream::read
- Purpose: Reads from memory buffer
- Calls: None

## Globals
- **K_HEIGHT_MAP_VERSION_1-4 (const int)**: Height map version constants
- **K_BLEND_TILE_VERSION_
