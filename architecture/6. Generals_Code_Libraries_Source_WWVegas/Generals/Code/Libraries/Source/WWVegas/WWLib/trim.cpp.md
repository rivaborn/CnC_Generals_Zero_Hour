# Generals/Code/Libraries/Source/WWVegas/WWLib/trim.cpp

## Purpose
Provides string trimming utilities for both char and wchar_t strings.

## Responsibilities
- Trims leading and trailing whitespace from strings in-place
- Supports both narrow (char) and wide (wchar_t) character strings
- Handles NULL input safely

## Key Types
None

## Key Functions
### strtrim
- Purpose: Trims leading and trailing whitespace from a char string in-place
- Calls: isspace, strlen, strcpy

### wcstrim
- Purpose: Trims leading and trailing whitespace from a wchar_t string in-place
- Calls: iswspace, wcslen, wcscpy

## Globals
None

## Dependencies
- "always.h", "trim.h", <ctype.h>, <stddef.h>, <string.h>
- _UNIX: <wctype.h>
- isspace, iswspace, strlen, wcslen, strcpy, wcscpy
