# Generals/Code/GameEngine/Source/Common/System/AsciiString.cpp

## Purpose
This file implements the `AsciiString` class, a general-purpose string class for handling ASCII strings in the game engine.

## Responsibilities
- Manages string data with reference counting.
- Provides methods for string manipulation, including concatenation, trimming, and case conversion.
- Supports formatted string creation using variadic arguments.
- Implements tokenization of strings based on specified separators.

## Key Types
- `AsciiString`: A class for handling ASCII strings with reference-counted memory management.
- `AsciiStringData`: A struct containing the actual string data and metadata (reference count, allocated size).

## Key Functions
### skipSeps
- Purpose: Skips over characters in a string that are present in a given set of separators.
- Calls: `strchr`

### skipNonSeps
- Purpose: Skips over characters in a string that are not present in a given set of separators.
- Calls: `strchr`

### skipWhitespace
- Purpose: Skips over whitespace characters in a string.
- Calls: `isspace`

### skipNonWhitespace
- Purpose: Skips over non-whitespace characters in a string.
- Calls: `isspace`

## Globals
- `TheEmptyString (AsciiString)`: A static instance representing an empty string.

## Dependencies
- Key includes:
  - `"PreRTS.h"`
  - `"Common/CriticalSection.h"`

- External symbols used but not defined here:
  - `strchr`
  - `isspace`
  - `strcpy`
  - `strcat`
  - `strlen`
  - `tolower`
  - `_vsnprintf`
  - `stricmp`
  - `strnicmp`
  - `TheAsciiStringCriticalSection`
  - `TheDynamicMemoryAllocator`
