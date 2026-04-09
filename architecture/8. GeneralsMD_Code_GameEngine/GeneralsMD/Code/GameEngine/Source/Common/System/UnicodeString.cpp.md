# GeneralsMD/Code/GameEngine/Source/Common/System/UnicodeString.cpp

## Purpose
Implements a Unicode string class with reference counting and thread-safe operations for the game engine.

## Responsibilities
- Manages Unicode string storage with copy-on-write semantics
- Provides string manipulation (concat, trim, format, tokenization)
- Handles memory allocation/deallocation via a dynamic memory allocator
- Supports thread-safe operations using critical sections
- Converts between ASCII and Unicode strings

## Key Types
- `UnicodeString` (Class): Reference-counted Unicode string with copy-on-write
- `UnicodeStringData` (Struct): Internal data structure holding string buffer and refcount
- `WideChar` (Type): Alias for wchar_t (UTF-16 character)

## Key Functions
### `ensureUniqueBufferOfSize`
- Purpose: Allocates or reallocates a unique buffer of specified size
- Calls: `TheDynamicMemoryAllocator->allocateBytesDoNotZero`, `wcscpy`, `wcscat`, `releaseBuffer`

### `format_va`
- Purpose: Formats a string using variadic arguments
- Calls: `_vsnwprintf`, `set`

### `nextToken`
- Purpose: Extracts the next token from the string based on delimiters
- Calls: `wcsspn`, `wcscspn`, `getBufferForRead`, `memcpy`, `set`, `clear`

## Globals
- `TheEmptyString` (UnicodeString): Static empty string instance
- `TheUnicodeStringCriticalSection` (CriticalSection): Global critical section for thread safety
- `TheDynamicMemoryAllocator` (DynamicMemoryAllocator): Global memory allocator instance

## Dependencies
- `Common/CriticalSection.h` for thread synchronization
- `PreRTS.h` for engine precompilation
- `AsciiString` class for ASCII-Unicode conversion
- Windows API functions: `wcslen`, `wcscpy`, `wcscat`, `wcsspn`, `wcscspn`, `_vsnwprintf`
- Custom error codes: `ERROR_OUT_OF_MEMORY`
