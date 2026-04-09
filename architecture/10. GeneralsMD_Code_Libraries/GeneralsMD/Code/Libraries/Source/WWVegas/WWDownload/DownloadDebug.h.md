# GeneralsMD/Code/Libraries/Source/WWVegas/WWDownload/DownloadDebug.h

## Purpose
Header file providing debug utilities for download-related functionality, conditionally compiled based on debug builds.

## Responsibilities
- Declares debug logging and crash functions
- Provides macros for debug assertions and crash handling
- Manages a global flag for ignoring crashes

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
- Uses `extern "C"` linkage for C++ compatibility
