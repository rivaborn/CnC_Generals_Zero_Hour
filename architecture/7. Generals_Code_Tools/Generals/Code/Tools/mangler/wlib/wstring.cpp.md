# Generals/Code/Tools/mangler/wlib/wstring.cpp

## Purpose
Implements a custom string class (`Wstring`) for the game's toolchain, providing string manipulation operations.

## Responsibilities
- String construction, copying, and destruction
- Concatenation, insertion, and removal of substrings
- Case conversion and formatting
- Tokenization and line extraction
- Memory management for string storage

## Key Types
- `Wstring` (Class): Custom string class with dynamic memory management
- `PADSIZE` (const): Padding size for memory allocation (32 bytes)

## Key Functions
### `Wstring::operator+`
- Purpose: Concatenates two strings
- Calls: `cat`

### `Wstring::replace`
- Purpose: Replaces all occurrences of a substring with another
- Calls: `strstr`, `cat`, `set`

### `Wstring::setFormatted`
- Purpose: Formats a string using `printf`-style arguments
- Calls: `new`, `va_start`, `vsprintf`, `va_end`, `set`, `delete[]`

### `Wstring::getToken`
- Purpose: Extracts a token delimited by specified characters
- Calls: `strchr`, `set`, `truncate`

### `Wstring::strgrow`
- Purpose: Ensures the string has sufficient allocated memory
- Calls: `new`, `strcpy`, `delete[]`

## Globals
- None

## Dependencies
- `<ctype.h>`, `<stdlib.h>`, `<stdio.h>`, `<string.h>`, `<stdarg.h>`
- `wstring.h` (header for `Wstring` class)
- `strcpy`, `strcat`, `strlen`, `strcmp`, `strncpy`, `strncat`, `memmove`, `memset`, `strchr`, `strstr`, `tolower`, `toupper`, `vsprintf`
