# Generals/Code/Libraries/Source/WWVegas/WWLib/strtok_r.h

## Purpose
Header file declaring a reentrant string tokenization function for Windows platforms.

## Responsibilities
- Declares `strtok_r` for Windows compatibility
- Conditionally includes the declaration based on platform
- Prevents multiple inclusions via header guards

## Key Types
- None

## Key Functions
### strtok_r
- Purpose: Tokenizes a string using specified delimiters in a reentrant manner.
- Calls: Not inferable (declaration only)

## Globals
- None

## Dependencies
- Platform-specific macros (`_MSC_VER`, `_UNIX`)
- Header guards (`__STRTOK_R_H__`)
