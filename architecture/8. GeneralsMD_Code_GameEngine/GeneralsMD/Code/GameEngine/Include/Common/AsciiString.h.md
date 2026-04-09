# GeneralsMD/Code/GameEngine/Include/Common/AsciiString.h

## Purpose
Defines the `AsciiString` class, a reference-counted string type for the Generals game engine.

## Responsibilities
- Provides a string class with MFC CString-like behavior
- Manages memory automatically via reference counting
- Supports common string operations (concatenation, comparison, formatting)
- Ensures thread-safe reference counting using `InterlockedIncrement/Decrement`

## Key Types
- **AsciiString (Class)**: Main string class with reference-counted buffer
- **AsciiStringData (Struct)**: Internal data structure holding refcount and buffer
- **(anonymous enum)**: Contains `MAX_FORMAT_BUF_LEN` and `MAX_LEN` constants
- **UnicodeString (Class)**: Forward-declared Unicode string class

## Key Functions
### `AsciiString::ensureUniqueBufferOfSize`
- Purpose: Allocates or reallocates buffer to ensure specified size
- Calls: `freeBytes`, memory allocation functions

### `AsciiString::format`
- Purpose: Formats string using `sprintf`-style arguments
- Calls: `format_va`, `va_start`, `va_end`

### `AsciiString::concat`
- Purpose: Appends string/char to the end
- Calls: `ensureUniqueBufferOfSize`, `strlen`

## Globals
- **TheEmptyString (AsciiString)**: Static empty string instance
- **TheAsciiStringCriticalSection (CriticalSection)**: Thread synchronization object

## Dependencies
- `<stdarg.h>`, `<stdio.h>`, `<string.h>`
- `Lib/BaseType.h`, `Common/Debug.h`, `Common/Errors.h`
- `Windows.h` for `InterlockedIncrement/Decrement`
- `UnicodeString` (forward-declared)
