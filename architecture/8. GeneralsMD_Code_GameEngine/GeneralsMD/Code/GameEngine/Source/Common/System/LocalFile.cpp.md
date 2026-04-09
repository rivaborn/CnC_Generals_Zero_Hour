# GeneralsMD/Code/GameEngine/Source/Common/System/LocalFile.cpp

## Purpose
Implements file I/O operations for local filesystem access in the SAGE engine.

## Responsibilities
- Provides buffered and unbuffered file operations
- Manages file handles/stream objects
- Supports reading/writing, seeking, and scanning data
- Tracks open file count for debugging
- Converts local files to RAM-based files

## Key Types
- **LocalFile (Class)**: Wraps local filesystem operations
- **s_totalOpen (Int)**: Tracks number of open files

## Key Functions
### LocalFile::open
- Purpose: Opens a file with specified access flags
- Calls: File::open, fopen/_open, seek

### LocalFile::read
- Purpose: Reads data from file into buffer
- Calls: fread/_read, _lseek/fseek

### LocalFile::write
- Purpose: Writes data from buffer to file
- Calls: fwrite/_write

### LocalFile::seek
- Purpose: Changes file position
- Calls: fseek/_lseek, ftell

### LocalFile::scanInt
- Purpose: Reads integer value from file
- Calls: fread/_read, fseek/_lseek

### LocalFile::scanReal
- Purpose: Reads floating-point value from file
- Calls: fread/_read, fseek/_lseek

### LocalFile::convertToRAMFile
- Purpose: Converts local file to RAM-based file
- Calls: RAMFile::open, File::close

### LocalFile::readEntireAndClose
- Purpose: Reads entire file into memory and closes it
- Calls: File::size, File::read, File::close

## Globals
- **s_totalOpen (Int)**: Tracks number of open files

## Dependencies
- Common/LocalFile.h
- Common/RAMFile.h
- Lib/BaseType.h
- Common/PerfTimer.h
- C runtime functions (fopen, fclose, fread, fwrite, fseek, ftell, _open, _close, _read, _write, _lseek, _S_IREAD, _S_IWRITE)
