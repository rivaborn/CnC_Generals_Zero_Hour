# Generals/Code/Libraries/Source/WWVegas/WWLib/widestring.cpp

## Purpose
Implements a wide string class for Unicode string handling with memory management optimizations.

## Responsibilities
- Manages wide string allocation and deallocation
- Provides temporary string buffers for performance
- Supports string formatting and resizing
- Handles thread-safe temporary string management

## Key Types
- `WideStringClass`: Main class for wide string operations
- `CriticalSectionClass`: Thread synchronization for temp string access
- `_HEADER` (struct): Internal buffer header (not shown in file)

## Key Functions
### `Get_String`
- Purpose: Allocates or reuses a string buffer based on length and temp flag
- Calls: `CriticalSectionClass::LockClass`, `Set_Buffer_And_Allocated_Length`, `Allocate_Buffer`

### `Resize`
- Purpose: Resizes the string buffer if needed
- Calls: `Get_Allocated_Length`, `Allocate_Buffer`, `Set_Buffer_And_Allocated_Length`

### `Uninitialised_Grow`
- Purpose: Grows the buffer without initializing new memory
- Calls: `Get_Allocated_Length`, `Allocate_Buffer`, `Set_Buffer_And_Allocated_Length`

### `Free_String`
- Purpose: Releases string memory or returns temp buffer to pool
- Calls: `CriticalSectionClass::LockClass`

### `Format_Args`
- Purpose: Formats a string using va_list
- Calls: `_vsnwprintf`

### `Format`
- Purpose: Variadic wrapper for string formatting
- Calls: `va_start`, `_vsnwprintf`, `va_end`

## Globals
- `m_UsedTempStringCount` (int): Tracks active temp string count
- `m_TempMutex` (CriticalSectionClass): Sync for temp string access
- `m_NullChar` (WCHAR): Null terminator
- `m_EmptyString` (WCHAR*): Points to null char
- `m_TempString1-4` (char[]): Stack-allocated temp buffers
- `m_FreeTempPtr` (WCHAR*[]): Available temp buffer pointers
- `m_ResTempPtr` (WCHAR*[]): Reserved temp buffer pointers

## Dependencies
- `widestring.h`: Class declaration
- `win.h`: Windows API headers
- `<stdio.h>`: For formatting functions
- `CriticalSectionClass`: Thread synchronization
- `_vsnwprintf`: Wide char formatting
