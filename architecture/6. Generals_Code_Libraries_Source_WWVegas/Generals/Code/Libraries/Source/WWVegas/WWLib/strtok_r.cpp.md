# Generals/Code/Libraries/Source/WWVegas/WWLib/strtok_r.cpp

## Purpose
Implements a thread-safe version of `strtok` (reentrant `strtok_r`) for Windows platforms.

## Responsibilities
- Provides a reentrant string tokenization function.
- Avoids using internal static variables (unlike standard `strtok`).
- Handles delimiter-based string splitting with a user-provided state pointer.

## Key Types
- None

## Key Functions
### strtok_r
- Purpose: Tokenizes a string using specified delimiters, maintaining state via a user-provided pointer.
- Calls: `strcspn`, `strspn`

## Globals
- None

## Dependencies
- `strtok_r.h` (header)
- `<string.h>` (for `strcspn`, `strspn`)
- `<stdio.h>` (likely for `NULL` or other standard types)
