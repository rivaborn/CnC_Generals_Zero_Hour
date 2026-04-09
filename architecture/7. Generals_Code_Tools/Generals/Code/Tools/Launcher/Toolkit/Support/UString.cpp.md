# Generals/Code/Tools/Launcher/Toolkit/Support/UString.cpp

## Purpose
Implements a Unicode string management class (UString) with various string manipulation functions.

## Responsibilities
- Unicode string storage and manipulation
- Character case conversion (upper/lower)
- String trimming and substring extraction
- ANSI/Unicode string conversion
- Memory management for string data

## Key Types
- **UString (Class)**: Unicode string container with various manipulation methods
- **CharToLower (template function)**: Converts character to lowercase
- **CharToUpper (template function)**: Converts character to uppercase
- **IsCharacter (template function)**: Checks if character exists in a set
- **StripLeft (template function)**: Removes leading characters
- **StripRight (template function)**: Removes trailing characters

## Key Functions
### UString::Copy
- Purpose: Copies string data from various sources (ANSI, Unicode, UString)
- Calls: AllocString, strlen, wcslen, wcscpy

### UString::Trim
- Purpose: Removes leading/trailing characters
- Calls: TrimLeft, TrimRight

### UString::ToUpper/ToLower
- Purpose: Converts entire string to upper/lower case
- Calls: wcsupr, wcslwr

### UString::Resize
- Purpose: Resizes string capacity
- Calls: new, wcsncpy, delete

## Globals
- None

## Dependencies
- VisualC.h, UString.h, StringConvert.h
- <string.h>, <stdlib.h>, <assert.h>
- Uses wcscpy, wcslwr, wcsupr, wcslen, wcsrev from C runtime
