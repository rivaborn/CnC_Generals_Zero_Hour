# Generals/Code/Tools/CRCDiff/debug.cpp

## Purpose
Provides minimal debug logging functionality for the CRCDiff tool.

## Responsibilities
- Implements a debug logging function
- Outputs messages to console and debug string
- Handles variable argument formatting

## Key Types
- None

## Key Functions
### DebugLog
- Purpose: Logs formatted debug messages to console and debug output.
- Calls: `vsnprintf`, `printf`, `OutputDebugString`

## Globals
- `buffer` (char[1024]): Static buffer for formatting debug messages

## Dependencies
- `<windows.h>` for `OutputDebugString`
- `<cstdio>` for `printf`/`vsnprintf`
- `debug.h` for function declaration
- `va_list`/`va_start`/`va_end` for variadic argument handling
