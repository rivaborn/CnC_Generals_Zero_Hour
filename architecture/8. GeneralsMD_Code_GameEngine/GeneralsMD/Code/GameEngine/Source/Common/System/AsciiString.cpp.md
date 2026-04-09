# GeneralsMD/Code/GameEngine/Source/Common/System/AsciiString.cpp

## Purpose
Implements the AsciiString class, providing string manipulation utilities for the game engine.

## Responsibilities
- String buffer management (allocation, reference counting)
- Text processing (trimming, case conversion, formatting)
- Tokenization and substring checks
- Memory validation in debug builds

## Key Types
- AsciiString (Class): Reference-counted ASCII string container
- AsciiStringData (Struct): Internal buffer storage with refcounting
- TheEmptyString (Static): Singleton empty string instance

## Key Functions
### skipSeps
- Purpose: Advances pointer past separator characters
- Calls: strchr

### skipNonSeps
- Purpose: Advances pointer past non-separator characters
- Calls: strchr

### skipWhitespace
- Purpose: Advances pointer past whitespace characters
- Calls: isspace

### skipNonWhitespace
- Purpose: Advances pointer past non-whitespace characters
- Calls: isspace

### ensureUniqueBufferOfSize
- Purpose: Ensures string has unique buffer of specified size
- Calls: TheDynamicMemoryAllocator methods, strcpy, strcat

### trim
- Purpose: Removes leading/trailing whitespace
- Calls: skipWhitespace, strlen, isspace

### format
- Purpose: Formats string using printf-style arguments
- Calls: format_va, va_start/va_end

### nextToken
- Purpose: Extracts next token from string using separators
- Calls: skipSeps, skipNonSeps, getBufferForRead

## Globals
- TheEmptyString (AsciiString): Singleton empty string instance
- MAX_LEN (const): Maximum string length constant

## Dependencies
- PreRTS.h, CriticalSection.h
- strchr, isspace, strlen, strcpy, strcat, strncmp, strnicmp
- TheDynamicMemoryAllocator (external memory manager)
- UnicodeString (for translation)
- DEBUG_ASSERTCRASH, DEBUG_LOG (debug utilities)
