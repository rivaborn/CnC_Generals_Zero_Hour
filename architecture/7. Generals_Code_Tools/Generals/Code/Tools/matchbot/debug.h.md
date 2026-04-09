# Generals/Code/Tools/matchbot/debug.h

## Purpose
Header file providing conditional debug logging functionality for the matchbot tool.

## Responsibilities
- Defines `DEBUG_LOG` macro for conditional debug output
- Declares `DebugLog` function for formatted debug messages
- Handles C/C++ compatibility for the debug interface

## Key Types
- None

## Key Functions
### DebugLog
- Purpose: Outputs formatted debug messages when DEBUG is defined
- Calls: `va_list` handling (not visible in header)

## Globals
- None

## Dependencies
- `<cstdarg>` for variable argument handling
- Conditional compilation based on `DEBUG` macro
