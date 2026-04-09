# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/wwstring.h

## Purpose
Defines the `StringClass` for Unicode-friendly string manipulation in the SAGE engine.

## Responsibilities
- Provides string construction, comparison, and manipulation
- Supports temporary string optimization
- Handles Unicode (TCHAR/WCHAR) strings
- Manages memory allocation/deallocation for strings

## Key Types
- **StringClass (Class)**: Main string class with operators and methods
- **HEADER (Struct)**: Internal header storing allocated/used length
- **MAX_TEMP_STRING (Enum)**: Max temporary strings (8)
- **MAX_TEMP_LEN (Enum)**: Max temp string length (256)
- **MAX_TEMP_BYTES (Enum)**: Max temp string bytes
- **ALL_TEMP_STRINGS_USED_MASK (Enum)**: Mask for temp strings

## Key Functions
### StringClass::operator= (const StringClass &string)
- Purpose: Assigns one StringClass to another
- Calls: Uninitialised_Grow, Store_Length, memcpy

### StringClass::operator+= (const TCHAR *string)
- Purpose: Appends a TCHAR string to the end
- Calls: Get_Length, _tcslen, Resize, Store_Length, memcpy

### StringClass::Format
- Purpose: Formats a string using printf-style arguments
- Calls: Get_Buffer, Format_Args

### StringClass::Trim
- Purpose: Trims leading/trailing whitespace
- Calls: strtrim

## Globals
- **ReservedMask (unsigned)**: Tracks temp string usage
- **m_TempStrings (char[])**: Pool for temporary strings
- **m_Mutex (FastCriticalSectionClass)**: Thread synchronization
- **m_NullChar (TCHAR)**: Null terminator
- **m_EmptyString (TCHAR*)**: Empty string pointer

## Dependencies
- **always.h**, **mutex.h**, **win.h**, **string.h**, **stdarg.h**, **tchar.h**, **trim.h**, **wwdebug.h**
- **W3DNEWARRAY** (memory allocation)
- **_tcscmp**, **_tcslen**, **_tcsicmp**, **memcpy**, **memmove** (C runtime)
