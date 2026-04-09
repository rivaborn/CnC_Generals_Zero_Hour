# Generals/Code/Tools/matchbot/wlib/wstring.cpp

## Purpose
Implements a string class (`Wstring`) for the matchbot tool, providing string manipulation operations.

## Responsibilities
- String construction, copying, and destruction
- String comparison and concatenation
- Character/string insertion, removal, and replacement
- Case conversion and formatting
- Tokenization and line extraction

## Key Types
- `Wstring` (Class): String wrapper with dynamic memory management
- `bit8` (Type): Boolean-like type (0/1)
- `sint32`/`uint32` (Types): Signed/unsigned 32-bit integers

## Key Functions
### `Wstring::operator+`
- Purpose: Concatenates strings
- Calls: `cat`

### `Wstring::replace`
- Purpose: Replaces all occurrences of a substring
- Calls: `strstr`, `cat`, `set`

### `Wstring::setFormatted`
- Purpose: Formats string using `printf`-style arguments
- Calls: `new`, `va_start`, `vsprintf`, `va_end`, `set`, `delete[]`

### `Wstring::getToken`
- Purpose: Extracts a token delimited by specified characters
- Calls: `strchr`, `set`, `truncate`

### `Wstring::strgrow`
- Purpose: Ensures string buffer has sufficient capacity
- Calls: `new`, `strcpy`, `delete[]`

## Globals
- `PADSIZE` (const int): Padding size for memory allocation (32)

## Dependencies
- `<ctype.h>`, `<stdlib.h>`, `<stdio.h>`, `<string.h>`, `<stdarg.h>`
- `wstring.h` (header for `Wstring` class)
- `strcpy`, `strcat`, `strlen`, `strcmp`, `strncpy`, `strncat`, `memmove`, `memset`, `strchr`, `strstr`, `tolower`, `toupper`, `vsprintf`
