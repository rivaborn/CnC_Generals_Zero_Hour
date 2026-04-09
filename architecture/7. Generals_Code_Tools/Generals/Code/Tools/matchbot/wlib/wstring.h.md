# Generals/Code/Tools/matchbot/wlib/wstring.h

## Purpose
Defines a string utility class for the matchbot tool, providing string manipulation and formatting capabilities.

## Responsibilities
- String construction, copying, and destruction
- String concatenation, insertion, and removal
- String formatting and case conversion
- Token and line extraction
- Comparison and assignment operators

## Key Types
- Wstring (Class): A string wrapper with dynamic memory management and manipulation methods

## Key Functions
### Wstring::setFormatted
- Purpose: Formats a string using printf-style formatting
- Calls: Not inferable

### Wstring::beautifyNumber
- Purpose: Formats a number with commas as thousand separators
- Calls: Not inferable

### Wstring::getToken
- Purpose: Extracts a token from the string based on delimiters
- Calls: Not inferable

### Wstring::getLine
- Purpose: Extracts a line from the string
- Calls: Not inferable

## Globals
- None

## Dependencies
- `<stdio.h>`
- `<stdlib.h>`
- `"wstypes.h"` (for bit8, uint32, sint32, etc.)
- Uses variadic functions (for setFormatted)
