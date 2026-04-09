# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/wwstring.cpp

## Purpose
Implements the StringClass for string manipulation with memory management and thread safety.

## Responsibilities
- Manages string allocation, resizing, and deallocation
- Provides formatted string operations
- Handles temporary string buffers with thread synchronization
- Supports Unicode and ANSI character conversions

## Key Types
- StringClass: Main string class with buffer management
- _HEADER: Internal header structure for string buffers (not shown in snippet)
- FastCriticalSectionClass: Thread synchronization primitive

## Key Functions
### Get_String
- Purpose: Allocates or reuses a string buffer based on length and temporary flag
- Calls: Allocate_Buffer, Set_Buffer_And_Allocated_Length, Free_String

### Resize
- Purpose: Resizes the string buffer while preserving content
- Calls: Allocate_Buffer, Set_Buffer_And_Allocated_Length

### Uninitialised_Grow
- Purpose: Resizes buffer without preserving content
- Calls: Allocate_Buffer, Set_Buffer_And_Allocated_Length, Store_Length

### Free_String
- Purpose: Releases string buffer resources
- Calls: None (direct memory operations)

### Format_Args
- Purpose: Formats string using va_list arguments
- Calls: _vsnwprintf/_vsnprintf (platform dependent)

### Copy_Wide
- Purpose: Converts wide string to multi-byte format
- Calls: WideCharToMultiByte

## Globals
- m_Mutex (FastCriticalSectionClass): Thread synchronization for temp strings
- m_NullChar (TCHAR): Null terminator
- m_EmptyString (TCHAR*): Points to null terminator
- m_TempStrings (char[]): Pool of temporary string buffers
- ReservedMask (unsigned): Bitmask tracking temp string usage

## Dependencies
- wwstring.h: Header for StringClass
- win.h: Windows API headers
- wwmemlog.h: Memory logging macros
- mutex.h: Thread synchronization primitives
- <stdio.h>: For vsnprintf family functions
