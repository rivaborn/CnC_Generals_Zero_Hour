# Generals/Code/Libraries/Source/WWVegas/WWLib/widestring.h

## Purpose
Defines the `WideStringClass` for Unicode string manipulation in the SAGE engine.

## Responsibilities
- Provides Unicode string operations (construction, comparison, concatenation)
- Manages dynamic memory for wide character strings
- Supports conversion between Unicode and ANSI strings
- Implements temporary string pooling for performance

## Key Types
- **WideStringClass (Class)**: Unicode string wrapper with dynamic memory management
- **HEADER (Struct)**: Internal header storing string length and allocation size
- **(anonymous enum)**: Constants for temporary string pool limits

## Key Functions
### WideStringClass::operator const wchar_t *
- Purpose: Allows implicit conversion to `const wchar_t*`
- Calls: None

### operator+ (overloads)
- Purpose: Concatenates wide strings
- Calls: `WideStringClass` constructor, `operator+=`

### WideStringClass::Convert_From
- Purpose: Converts ANSI string to Unicode
- Calls: `Uninitialised_Grow`, `strlen`

### WideStringClass::Convert_To
- Purpose: Converts Unicode string to ANSI
- Calls: `StringClass::Get_Buffer`

## Globals
- **m_TempString1-4 (char[])**: Temporary string buffers
- **m_FreeTempPtr/ResTempPtr (WCHAR*)**: Temporary string pool pointers
- **m_UsedTempStringCount (int)**: Count of used temporary strings
- **m_TempMutex (CriticalSectionClass)**: Mutex for thread safety
- **m_NullChar (WCHAR)**: Null terminator
- **m_EmptyString (WCHAR*)**: Empty string pointer

## Dependencies
- `<string.h>`, `<stdarg.h>`, `<wchar.h>`
- `always.h`, `wwdebug.h`, `win.h`, `wwstring.h`
- `CriticalSectionClass`, `StringClass`, `W3DNEWARRAY`
