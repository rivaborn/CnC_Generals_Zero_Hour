# Generals/Code/Tools/Launcher/wstring.cpp

## Purpose
Implements a custom string class (`Wstring`) for the game's toolchain, providing string manipulation operations.

## Responsibilities
- String construction, copying, and destruction
- Concatenation and insertion operations
- Character/string removal and replacement
- Case conversion and truncation
- Tokenization and line extraction

## Key Types
- **Wstring (Class)**: Custom string wrapper managing dynamic char arrays
- **bit8 (Type)**: Boolean-like type (0/1) for return values

## Key Functions
### `operator==`
- Purpose: Compares string equality with another string or Wstring
- Calls: `strcmp`

### `cat`
- Purpose: Appends a string to the current string
- Calls: `strlen`, `strcpy`, `strcat`, `new`, `delete[]`

### `remove`
- Purpose: Removes characters at a specified position
- Calls: `strlen`, `new`, `strcpy`, `strcat`, `delete[]`

### `replace`
- Purpose: Replaces all occurrences of a substring
- Calls: `strstr`, `strlen`, `cat`

### `getToken`
- Purpose: Extracts a token delimited by specified characters
- Calls: `strchr`, `strlen`, `set`, `truncate`

## Globals
- None

## Dependencies
- `<ctype.h>`, `<stdlib.h>`, `<stdio.h>`, `<string.h>`
- `wstring.h` (header for Wstring class)
- External symbols: `strlen`, `strcpy`, `strcat`, `strchr`, `strstr`, `memmove`, `memset`, `tolower`, `toupper`
