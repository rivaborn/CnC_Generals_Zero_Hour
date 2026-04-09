# Generals/Code/Libraries/Source/WWVegas/WWDownload/DownloadDebug.h

## Purpose
Header file for debug utilities in the download subsystem, providing crash and log functions.

## Responsibilities
- Defines debug logging and crash macros
- Conditionally includes debug functions based on build flags
- Provides a global variable for crash handling control

## Key Types
None

## Key Functions
### DebugCrash
- Purpose: Triggers a debug crash with a formatted message
- Calls: Not inferable

### DebugLog
- Purpose: Logs a debug message with formatted output
- Calls: Not inferable

## Globals
- TheCurrentIgnoreCrashPtr (char*): Tracks whether crashes should be ignored

## Dependencies
- `<stdarg.h>` for variadic function support
- Build flags: `NDEBUG`, `DISABLE_DEBUG_LOGGING`
