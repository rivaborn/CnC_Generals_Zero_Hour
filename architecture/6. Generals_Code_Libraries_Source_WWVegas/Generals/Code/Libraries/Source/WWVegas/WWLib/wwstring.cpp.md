# Generals/Code/Libraries/Source/WWVegas/WWLib/wwstring.cpp

## Purpose
Implements the `StringClass` for string manipulation with memory management and thread safety.

## Responsibilities
- Manages string allocation/deallocation (stack/heap/temporary buffers)
- Provides formatted string operations
- Handles thread synchronization for temporary string buffers
- Tracks memory usage via `WWMEMLOG`
- Supports Unicode/ANSI builds

## Key Types
- `StringClass` (Class): Main string wrapper with buffer management
- `_HEADER` (Struct): Internal buffer header (not shown in snippet)
- `CriticalSectionClass` (Class): Thread synchronization primitive

## Key Functions
### `Get_String`
- Purpose: Allocates or reuses a string buffer (temporary or permanent).
- Calls: `WWMEMLOG`, `Allocate_Buffer`, `Set_Buffer_And_Allocated_Length`

### `Resize`
- Purpose: Resizes the string buffer if needed, preserving content.
- Calls: `WWMEMLOG`, `Allocate_Buffer`, `_tcscpy`, `Set_Buffer_And_Allocated_Length`

### `Uninitialised_Grow`
- Purpose: Resizes the buffer without preserving content.
- Calls: `WWMEMLOG`, `Allocate_Buffer`, `Set_Buffer_And_Allocated_Length`

### `Free_String`
- Purpose: Releases string buffer (temporary or heap-allocated).
- Calls: `WWMEMLOG`, `delete []`

### `Format_Args`
- Purpose: Formats a string using a `va_list`.
- Calls: `_vsnwprintf`/`_vsnprintf` (platform-dependent)

### `Format`
- Purpose: Variadic wrapper for `Format_Args`.
- Calls: `va_start`, `va_end`, `Format_Args`

## Globals
- `m_Mutex` (CriticalSectionClass): Thread synchronization for temp buffers
- `m_NullChar` (TCHAR): Null terminator
- `m_EmptyString` (TCHAR*): Points to `m_NullChar`
- `m_TempStrings` (char[]): Pre-allocated temp buffer pool
- `ReservedMask` (unsigned): Bitmask tracking temp buffer usage

## Dependencies
- `wwstring.h`, `win.h`, `wwmemlog.h`, `mutex.h`
- `<stdio.h>` (for `_vsnprintf`/`_vsnwprintf`)
- `CriticalSectionClass::LockClass` (for mutex locking)
