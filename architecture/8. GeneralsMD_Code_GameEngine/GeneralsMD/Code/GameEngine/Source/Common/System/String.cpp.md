# GeneralsMD/Code/GameEngine/Source/Common/System/String.cpp

## Purpose
Implements the `WSYS_String` class, a custom string wrapper for the game engine.

## Responsibilities
- String construction, assignment, and comparison
- Concatenation and formatting operations
- Case conversion utilities

## Key Types
- `WSYS_String` (Class): A string wrapper with dynamic memory management
- `Char` (Type): Alias for character type (likely `char` or `wchar_t`)

## Key Functions
### `WSYS_String::operator+=`
- Purpose: Appends a string to the current instance
- Calls: `strlen`, `strcpy`, `strcat`, `delete []`

### `operator+ (const WSYS_String &, const WSYS_String &)`
- Purpose: Concatenates two `WSYS_String` instances
- Calls: `WSYS_String::operator+=`

### `WSYS_String::format`
- Purpose: Formats a string using `va_list`
- Calls: `vsprintf`, `set`

### `WSYS_String::set`
- Purpose: Sets the string content with dynamic allocation
- Calls: `strlen`, `strcpy`, `delete []`

## Globals
- None

## Dependencies
- `<stdio.h>`, `<stdlib.h>`, `<stdarg.h>`, `<string.h>`
- `Common/string.h` (header for `WSYS_String`)
- `MSGNEW` (memory allocation macro)
