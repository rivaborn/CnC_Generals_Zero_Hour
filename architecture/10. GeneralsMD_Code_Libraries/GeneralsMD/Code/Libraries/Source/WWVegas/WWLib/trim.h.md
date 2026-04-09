# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/trim.h

## Purpose
Header file declaring string trimming utility functions for C-style strings and wide strings.

## Responsibilities
- Declares `strtrim` for trimming C-style strings.
- Declares `wcstrim` for trimming wide strings.
- Provides header guards to prevent multiple inclusions.

## Key Types
- None

## Key Functions
### strtrim
- Purpose: Trims whitespace from the beginning and end of a C-style string.
- Calls: Not inferable (implementation not shown).

### wcstrim
- Purpose: Trims whitespace from the beginning and end of a wide string.
- Calls: Not inferable (implementation not shown).

## Globals
- None

## Dependencies
- `<wchar.h>`: For wide character support.
- Not inferable: Likely depends on standard C string manipulation functions (e.g., `isspace`, `strlen`).
