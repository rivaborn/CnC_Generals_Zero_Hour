# Generals/Code/Tools/Compress/Compress.cpp

## Purpose
Command-line tool for compressing files and checking compression types in the SAGE engine.

## Responsibilities
- Parse command-line arguments for input/output files and compression type
- Display help information and compression modes
- Check existing file compression type and statistics
- Compress files (stub implementation shown)

## Key Types
- None

## Key Functions
### ReleaseLog
- Purpose: Log messages in release builds using printf
- Calls: vsnprintf

### dumpHelp
- Purpose: Print usage instructions and available compression modes
- Calls: DEBUG_LOG, CompressionManager::getCompressionNameByType

### main
- Purpose: Entry point handling argument parsing and compression operations
- Calls: dumpHelp, stricmp, strcmp, CompressionManager::getPreferredCompression, CompressionManager::getCompressionNameByType, fopen, fseek, ftell, fread, CompressionManager::getCompressionType, CompressionManager::getUncompressedSize

## Globals
- None

## Dependencies
- <string>, <cstdio>, <cstdarg>
- Lib/BaseType.h
- Compression/Compression.h
- ../CRCDiff/Debug.h
- CompressionManager class (external)
