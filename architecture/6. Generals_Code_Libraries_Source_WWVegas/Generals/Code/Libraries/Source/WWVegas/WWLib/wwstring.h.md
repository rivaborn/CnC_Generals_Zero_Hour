# Generals/Code/Libraries/Source/WWVegas/WWLib/wwstring.h

## Purpose
Defines the `StringClass` for string manipulation, supporting both single-byte and double-byte (Unicode) characters.

## Responsibilities
- Provides string storage and manipulation
- Supports temporary string optimization
- Implements string comparison and concatenation
- Manages memory allocation/deallocation for strings
- Offers formatted string operations

## Key Types
- **StringClass (Class)**: Main string class with buffer management and operations
- **HEADER (Struct)**: Internal header storing allocated length and string length
- **(anonymous enum) (Enum)**: Constants for temporary string pool management

## Key Functions
### StringClass::operator const char *
- Purpose: Implicit conversion to const TCHAR*
- Calls: None

### operator+ (StringClass, StringClass)
- Purpose: Concatenates two StringClass objects
- Calls: StringClass constructor, operator+=

### operator+ (TCHAR*, StringClass)
- Purpose: Concatenates a TCHAR* with a StringClass
- Calls: StringClass constructor, operator+=

## Globals
- **ReservedMask (unsigned)**: Tracks usage of temporary string pool
- **m_TempStrings (char[])**: Pool for temporary string storage
- **m_Mutex (CriticalSectionClass)**: Synchronization for temporary string pool
- **m_NullChar (TCHAR)**: Null terminator character
- **m_EmptyString (TCHAR*)**: Pointer to empty string buffer

## Dependencies
- Key includes: `always.h`, `mutex.h`, `string.h`, `stdarg.h`, `tchar.h`, `wwdebug.h`
- External symbols: `W3DNEWARRAY`, `_tcslen`, `_tcscmp`, `_tcsicmp`, `memcpy`, `memmove`
