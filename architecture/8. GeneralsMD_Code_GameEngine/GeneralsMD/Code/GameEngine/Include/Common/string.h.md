# GeneralsMD/Code/GameEngine/Include/Common/string.h

## Purpose
Defines the `WSYS_String` class, a string wrapper for the SAGE engine.

## Responsibilities
- Provides string manipulation utilities
- Supports common string operations (concatenation, comparison, formatting)
- Manages string data allocation/deallocation
- Offers case conversion and length checks

## Key Types
- **WSYS_String (Class)**: A string class wrapping a `Char*` buffer with RAII semantics.

## Key Functions
### WSYS_String::operator const char *
- Purpose: Implicit conversion to `const Char*` for compatibility.
- Calls: None.

### WSYS_String::operator char *
- Purpose: Implicit conversion to `Char*` for compatibility.
- Calls: None.

### WSYS_String::format
- Purpose: Formats the string using `printf`-style arguments.
- Calls: Not inferable (likely internal formatting logic).

### WSYS_String::makeUpperCase / makeLowerCase
- Purpose: Converts the string to uppercase/lowercase in-place.
- Calls: Not inferable.

## Globals
- None.

## Dependencies
- `Lib/BaseType.h` (for `Char`, `Bool`, `Int` types)
- Uses variadic arguments (`...`) in `format`.
