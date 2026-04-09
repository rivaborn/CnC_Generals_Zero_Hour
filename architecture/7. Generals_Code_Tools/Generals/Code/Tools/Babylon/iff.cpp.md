# Generals/Code/Tools/Babylon/iff.cpp

## Purpose
Implements IFF (Interchange File Format) file handling for reading and writing chunked data structures.

## Responsibilities
- File I/O operations for IFF format
- Chunk and form navigation
- Memory-mapped and stream-based file access
- Endianness conversion for chunk headers

## Key Types
- IFF_FILE (struct): Main file handle with position tracking
- IFF_CHUNK (struct): Chunk header structure
- vIFF_ID_FORM (const): Form identifier constant

## Key Functions
### IFF_rawread
- Purpose: Reads data from file or memory buffer
- Calls: _read, memcpy

### IFF_seek
- Purpose: Seeks to position in file or memory buffer
- Calls: lseek

### IFF_Open
- Purpose: Opens IFF file for reading
- Calls: malloc, open

### IFF_Load
- Purpose: Loads entire file into memory
- Calls: malloc, open, lseek, DO_READ

### IFF_Read
- Purpose: Reads data from current chunk
- Calls: IFF_rawread

### IFF_New
- Purpose: Creates new IFF file for writing
- Calls: malloc, _open

### IFF_NewForm
- Purpose: Starts new form in output file
- Calls: DO_WRITE

### IFF_NewChunk
- Purpose: Starts new chunk in output file
- Calls: DO_WRITE

### IFF_Write
- Purpose: Writes data to current chunk
- Calls: _write

### IFF_CloseForm
- Purpose: Finalizes form writing with padding
- Calls: DO_WRITE, lseek

### IFF_CloseChunk
- Purpose: Finalizes chunk writing with padding
- Calls: DO_WRITE, lseek

## Globals
- None

## Dependencies
- stdAfx.h, sys/stat.h, iff.h
- Windows API: _open, _close, _read, _write, lseek
- Endianness conversion: BgEn32
- File I/O macros: DO_READ, DO_WRITE
