# Generals/Code/Tools/matchbot/debug.cpp

## Purpose
Provides minimal debug logging functionality for the matchbot tool.

## Responsibilities
- Implements debug logging via `DebugLog`
- Conditionally compiles debug features under `DEBUG` macro
- Platform-specific crash handling stubs
- Buffer management for formatted debug output

## Key Types
- None

## Key Functions
### DebugLog
- Purpose: Formats and outputs a debug message.
- Calls: `vsnprintf`, `DBGMSG`

### DebugCrash
- Purpose: Placeholder for crash handling (empty implementation).
- Calls: None

## Globals
- `TheCurrentIgnoreCrashPtr` (char*): Crash handling pointer (Windows only)
- `buffer` (static char[1024]): Temporary storage for formatted debug messages

## Dependencies
- `<wdebug.h>`: For `DBGMSG`
- `<cstdio>`: For `vsnprintf`
- `<stdarg.h>`: For variadic argument handling
- `debug.h`: Likely declares debug-related types/functions
