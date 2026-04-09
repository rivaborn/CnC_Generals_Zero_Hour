# Generals/Code/Tools/mangler/wlib/wstring.h

## Purpose
Header file defining the `Wstring` class, a custom string manipulation utility for the game's toolchain.

## Responsibilities
- Provides string construction, modification, and comparison operations
- Supports formatted string input and token/line parsing
- Manages dynamic string memory allocation
- Implements common string utilities (truncation, case conversion, etc.)

## Key Types
- **Wstring (Class)**: A dynamic string container with various manipulation methods

## Key Functions
### Wstring::setFormatted
- Purpose: Sets the string using a formatted input (printf-style)
- Calls: Not inferable

### Wstring::getToken
- Purpose: Extracts a token from the string at a given offset using a delimiter
- Calls: Not inferable

### Wstring::getLine
- Purpose: Extracts a line from the string at a given offset
- Calls: Not inferable

### Wstring::beautifyNumber
- Purpose: Formats a number string (e.g., adding commas)
- Calls: Not inferable

## Globals
- None

## Dependencies
- `<stdio.h>`
- `<stdlib.h>`
- `"wstypes.h"` (for `bit8`, `uint32`, etc.)
- Uses `RO` (Read-Only) attribute marker (likely from `wstypes.h`)
