# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/strtok_r.h

## Purpose
Header file declaring a reentrant version of strtok for Windows platforms.

## Responsibilities
- Declares `strtok_r` function for Windows
- Provides platform-specific conditional compilation
- Prevents multiple inclusions via header guards

## Key Types
None

## Key Functions
### strtok_r
- Purpose: Tokenizes a string using specified delimiters in a reentrant manner.
- Calls: Not inferable (declaration only)

## Globals
None

## Dependencies
- `_MSC_VER` (Microsoft compiler version check)
- `_UNIX` (platform detection macro)
- Standard C library headers (implied by strtok_r usage)
