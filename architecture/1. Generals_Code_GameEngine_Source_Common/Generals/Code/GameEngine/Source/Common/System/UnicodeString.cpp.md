# Generals/Code/GameEngine/Source/Common/System/UnicodeString.cpp

## Purpose
This file implements the `UnicodeString` class, which provides a general-purpose string handling mechanism for wide characters in the Command & Conquer Generals game engine.

## Responsibilities
- Manages Unicode strings with reference counting for efficient memory usage.
- Provides methods for string manipulation, including concatenation, trimming, and formatting.
- Handles buffer allocation and deallocation to ensure thread safety.

## Key Types
- `UnicodeString` (Class): Represents a wide character string with reference counting.
- `UnicodeStringData` (Struct): Internal data structure for managing the string buffer and metadata.

## Key Functions
### UnicodeString::ensureUniqueBufferOfSize
- Purpose: Ensures that the string has a unique buffer of sufficient size.
- Calls:
  - `wcscpy`
  - `wcscat`
  - `releaseBuffer`

### UnicodeString::releaseBuffer
- Purpose: Releases the current buffer if it is no longer needed.
- Calls:
  - `TheDynamicMemoryAllocator->freeBytes`

### UnicodeString::set
- Purpose: Sets the string to a new value, either from another `UnicodeString` or a wide character array.
- Calls:
  - `ensureUniqueBufferOfSize`
  - `releaseBuffer`

### UnicodeString::concat
- Purpose: Concatenates another wide character array to the end of the string.
- Calls:
  - `ensureUniqueBufferOfSize`

### UnicodeString::trim
- Purpose: Removes leading and trailing whitespace from the string.
- Calls:
  - `set`
  - `removeLastChar`

### UnicodeString::format
- Purpose: Formats the string using a format specifier and variable arguments.
- Calls:
  - `format_va`

### UnicodeString::nextToken
- Purpose: Extracts the next token from the string based on specified delimiters.
- Calls:
  - `wcsspn`
  - `wcscspn`
  - `memcpy`

## Globals
- `TheEmptyString` (UnicodeString): A static instance representing an empty Unicode string.

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/CriticalSection.h"
- External symbols used but not defined here:
  - `TheDynamicMemoryAllocator`
  - `TheUnicodeStringCriticalSection`
  - `ERROR_OUT_OF_MEMORY`
