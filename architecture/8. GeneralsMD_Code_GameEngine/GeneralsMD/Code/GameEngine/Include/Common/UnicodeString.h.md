# GeneralsMD/Code/GameEngine/Include/Common/UnicodeString.h

## Purpose
Defines the `UnicodeString` class, a reference-counted double-byte string type for the Generals codebase.

## Responsibilities
- Provides a string class with copy-on-write semantics
- Supports common string operations (concatenation, comparison, formatting)
- Manages memory automatically via reference counting
- Offers case-sensitive and case-insensitive comparison methods

## Key Types
- **UnicodeString (Class)**: Main string class with reference-counted buffer
- **UnicodeStringData (Struct)**: Internal data structure holding refcount and buffer
- **AsciiString (Class)**: Forward declaration for ASCII string conversion
- **(anonymous enum)**: Contains `MAX_FORMAT_BUF_LEN` and `MAX_LEN` constants

## Key Functions
### `operator==`, `operator!=`, `operator<`, `operator<=`, `operator>`, `operator>=`
- Purpose: Provide comparison operators for UnicodeString objects
- Calls: `wcscmp`, `_wcsicmp`

### `format`, `format_va`
- Purpose: Format strings using printf-style syntax
- Calls: `vsprintf`, internal buffer management

### `nextToken`
- Purpose: Extract whitespace-delimited tokens from the string
- Calls: Not inferable (implementation not shown)

## Globals
- **TheEmptyString (UnicodeString)**: Static empty string instance for efficiency

## Dependencies
- `<stdarg.h>`, `<stdio.h>`, `<string.h>`
- `Lib/BaseType.h`, `Common/Debug.h`, `Common/Errors.h`
- `wcscmp`, `_wcsicmp`, `wcslen`, `vsprintf` (C runtime functions)
