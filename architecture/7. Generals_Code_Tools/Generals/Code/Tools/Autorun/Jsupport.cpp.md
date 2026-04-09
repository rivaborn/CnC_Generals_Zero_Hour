# Generals/Code/Tools/Autorun/Jsupport.cpp

## Purpose
Provides DBCS (Double-Byte Character Set) text parsing utilities for Japanese text handling in the game.

## Responsibilities
- Validates DBCS characters at line boundaries
- Parses words in DBCS text
- Handles mixed single-byte and double-byte character sequences

## Key Types
None

## Key Functions
### IsDBCSInvalidAtTop
- Purpose: Checks if a DBCS character is invalid at the start of a line
- Calls: strchr

### IsDBCSInvalidAtEnd
- Purpose: Checks if a DBCS character is invalid at the end of a line
- Calls: strchr

### nGetWord
- Purpose: Parses the next word from a DBCS string, handling character boundaries
- Calls: IsDBCSLeadByte, IsDBCSInvalidAtTop, IsDBCSInvalidAtEnd

## Globals
- None

## Dependencies
- `<windows.h>` for Windows API types
- `jsupport.h` for function declarations
- `IsDBCSLeadByte` from Windows API (not defined here)
