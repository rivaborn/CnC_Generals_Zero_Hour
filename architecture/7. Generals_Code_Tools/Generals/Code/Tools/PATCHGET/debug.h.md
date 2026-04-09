# Generals/Code/Tools/PATCHGET/debug.h

## Purpose
Provides minimal debug utilities for logging and crash handling in the PATCHGET tool.

## Responsibilities
- Defines debug logging macros (`DEBUG_LOG`)
- Provides crash handling macros (`DEBUG_CRASH`, `DEBUG_ASSERTCRASH`)
- Manages a global crash ignore flag (`TheCurrentIgnoreCrashPtr`)

## Key Types
- None

## Key Functions
### DebugLog
- Purpose: Logs debug messages to output.
- Calls: `va_list` handling (via `cstdarg`)

### DebugCrash
- Purpose: Triggers a debug crash with a formatted message.
- Calls: Not inferable (external)

## Globals
- `TheCurrentIgnoreCrashPtr` (char*): Tracks whether crashes should be ignored.

## Dependencies
- `<cstdarg>` for variadic function support
- External `DebugCrash` function (declared but not defined)
