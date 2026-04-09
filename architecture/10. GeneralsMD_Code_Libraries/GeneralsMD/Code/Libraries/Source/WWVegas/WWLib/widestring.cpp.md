# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/widestring.cpp

## Purpose
Implements a wide string class for Unicode string handling in the game engine.

## Responsibilities
- Manages dynamic allocation and deallocation of wide strings
- Provides temporary string buffers for performance optimization
- Supports string formatting and conversion between ANSI and Unicode
- Handles thread-safe temporary string allocation

## Key Types
- `WideStringClass`: Main class for wide string operations
- `_HEADER` (struct): Internal header structure for memory management
- `FastCriticalSectionClass`: Thread synchronization primitive

## Key Functions
### `Get_String`
- Purpose: Allocates or reuses a string buffer based on length and temporary flag
- Calls: `FastCriticalSectionClass::LockClass`, `Allocate_Buffer`, `Set_Buffer_And_Allocated_Length`

### `Resize`
- Purpose: Resizes the string buffer if needed and copies existing content
- Calls: `Allocate_Buffer`, `Set_Buffer_And_Allocated_Length`

### `Uninitialised_Grow`
- Purpose: Grows the string buffer without initializing new memory
- Calls: `Allocate_Buffer`, `Set_Buffer_And_Allocated_Length`, `Store_Length`

### `Free_String`
- Purpose: Releases string memory or returns temporary buffer to pool
- Calls: `FastCriticalSectionClass::LockClass`

### `Format_Args`
- Purpose: Formats a wide string using a va_list
- Calls: `_vsnwprintf`

### `Convert_From`
- Purpose: Converts ANSI string to wide string
- Calls: `MultiByteToWideChar`, `Uninitialised_Grow`, `Store_Length`

## Globals
- `m_UsedTempStringCount` (int): Tracks number of used temporary buffers
- `m_TempMutex` (FastCriticalSectionClass): Mutex for thread-safe temp buffer access
- `m_EmptyString` (WCHAR*): Points to null character for empty strings
- `m_TempString1-4` (char[]): Stack-allocated temporary buffers
- `m_FreeTempPtr` (WCHAR*): Array of pointers to free temporary buffers
- `m_ResTempPtr` (WCHAR*): Array of pointers to reserved temporary buffers

## Dependencies
- `widestring.h`: Header for WideStringClass
- `win.h`: Windows API headers
- `<stdio.h>`: For printf-style functions
- `MultiByteToWideChar`: Windows API for character conversion
- `_vsnwprintf`: VS-style wide character formatting
