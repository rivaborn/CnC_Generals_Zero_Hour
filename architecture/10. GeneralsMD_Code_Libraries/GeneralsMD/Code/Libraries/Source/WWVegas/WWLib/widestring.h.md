# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/widestring.h

## Purpose
Defines the `WideStringClass` for Unicode string manipulation in the SAGE engine.

## Responsibilities
- Provides Unicode string operations (construction, comparison, concatenation)
- Manages dynamic memory for wide character strings
- Supports conversion between Unicode and ANSI strings
- Implements string formatting and trimming utilities
- Handles temporary string optimization via a pool system

## Key Types
- **WideStringClass (Class)**: Unicode string wrapper with dynamic memory management
- **_HEADER (Struct)**: Internal header storing allocated length and string length
- **HEADER (Struct)**: Alias for _HEADER
- **(anonymous enum)**: Constants for temporary string pool (MAX_TEMP_STRING, MAX_TEMP_LEN, MAX_TEMP_BYTES)

## Key Functions
### WideStringClass::operator const wchar_t *
- Purpose: Allows implicit conversion to `const wchar_t*`
- Calls: None

### operator+ (overloads)
- Purpose: Concatenates wide strings or wide strings with C-style strings
- Calls: `WideStringClass` constructor, `operator+=`

### WideStringClass::Format
- Purpose: Formats a wide string using `va_list`
- Calls: `Format_Args`

## Globals
- **m_TempString1-4 (char[])**: Temporary string buffers
- **m_FreeTempPtr / m_ResTempPtr (WCHAR*)**: Pointers for temporary string pool
- **m_UsedTempStringCount (int)**: Count of used temporary strings
- **m_TempMutex (FastCriticalSectionClass)**: Mutex for thread-safe temp string access
- **m_NullChar (WCHAR)**: Null terminator
- **m_EmptyString (WCHAR*)**: Empty string pointer

## Dependencies
- `<string.h>`, `<stdarg.h>`, `<wchar.h>`
- `always.h`, `wwdebug.h`, `win.h`, `wwstring.h`, `trim.h`
- `W3DNEWARRAY` (memory allocation)
- `wcscmp`, `wcslen`, `_wcsicmp`, `wcstrim` (C runtime)
