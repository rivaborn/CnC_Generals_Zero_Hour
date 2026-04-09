# Generals/Code/Tools/WW3D/pluglib/wwfile.h

## Purpose
Defines the `FileClass` abstract base class for file I/O operations in the WW3D plugin library.

## Responsibilities
- Declares virtual methods for file operations (open, read, write, seek, etc.)
- Provides printf-style formatted output methods
- Defines file access modes (READ, WRITE)
- Includes platform-specific macros for date/time handling

## Key Types
- **FileClass (Class)**: Abstract base class for file operations
- **(anonymous enum) (Enum)**: Contains READ, WRITE, and PRINTF_BUFFER_SIZE constants
- **READ (Enum)**: File read access mode
- **WRITE (Enum)**: File write access mode
- **PRINTF_BUFFER_SIZE (Enum)**: Buffer size for printf operations

## Key Functions
### Printf
- Purpose: Formatted output to file using stack buffer
- Calls: Not inferable (variadic function)

### Printf (overload)
- Purpose: Formatted output to file using supplied buffer
- Calls: Not inferable (variadic function)

### Printf_Indented
- Purpose: Formatted output with indentation
- Calls: Not inferable (variadic function)

## Globals
- **NULL (macro)**: Defined as 0 if not already defined
- **SEEK_SET/SEEK_CUR/SEEK_END (macros)**: File seek constants
- **YEAR/MONTH/DAY/HOUR/MINUTE/SECOND (macros)**: Date/time extraction macros

## Dependencies
- `osdep.h` (included for Unix)
- Standard C++ I/O concepts
- Variadic function handling (for printf methods)
