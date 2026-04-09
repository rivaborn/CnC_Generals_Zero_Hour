# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/trim.cpp

## Purpose
Provides string trimming utilities for both char and wchar_t strings.

## Responsibilities
- Trims leading and trailing whitespace from char strings
- Trims leading and trailing whitespace from wchar_t strings
- Modifies strings in-place

## Key Types
None

## Key Functions
### strtrim
- Purpose: Trims leading and trailing whitespace from a char string in-place
- Calls: strlen, strcpy

### wcstrim
- Purpose: Trims leading and trailing whitespace from a wchar_t string in-place
- Calls: wcslen, wcscpy

## Globals
None

## Dependencies
- "always.h"
- "trim.h"
- <string.h>
- <wctype.h> (on UNIX)
