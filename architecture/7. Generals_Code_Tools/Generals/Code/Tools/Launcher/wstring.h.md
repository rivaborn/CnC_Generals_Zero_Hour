# Generals/Code/Tools/Launcher/wstring.h

## Purpose
Defines a string utility class for the launcher tool, providing dynamic string manipulation.

## Responsibilities
- Manages dynamic string allocation and manipulation
- Provides string operations (concatenation, insertion, replacement)
- Supports case conversion and tokenization
- Implements comparison operators

## Key Types
- Wstring (Class): Dynamic string wrapper with manipulation methods

## Key Functions
### Wstring::cat
- Purpose: Concatenates strings or substrings
- Calls: None

### Wstring::replace
- Purpose: Replaces occurrences of one substring with another
- Calls: None

### Wstring::getToken
- Purpose: Extracts tokens from string using delimiters
- Calls: None

### Wstring::operator==
- Purpose: Compares strings for equality
- Calls: None

## Globals
- None

## Dependencies
- `<stdio.h>`, `<stdlib.h>`
- `wstypes.h` (for bit8, uint32, etc.)
- Uses custom types: bit8, uint32, sint32, char*
