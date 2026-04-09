# Generals/Code/Tools/PATCHGET/debug.cpp

## Purpose
Handles debug logging and crash reporting for the PATCHGET tool.

## Responsibilities
- Displays assertion failure dialogs with Abort/Retry/Ignore options
- Logs debug messages to OutputDebugString and console
- Manages crash ignore flags via global pointer
- Buffers formatted strings safely

## Key Types
- None

## Key Functions
### doCrashBox
- Purpose: Shows a crash dialog and handles user choice (Abort/Retry/Ignore)
- Calls: `MessageBox`, `DebugLog`, `_exit`, `DebugBreak`

### DebugLog
- Purpose: Formats and outputs debug messages to OutputDebugString and console
- Calls: `vsnprintf`, `OutputDebugString`, `printf`

### DebugCrash
- Purpose: Displays assertion failure dialog with formatted message and handles ignore persistence
- Calls: `strcat`, `vsprintf`, `OutputDebugString`, `printf`, `MessageBox`, `doCrashBox`

## Globals
- TheCurrentIgnoreCrashPtr (char*): Pointer to flag indicating whether to ignore crashes
- theBuffer (char[8192]): Static buffer for formatting debug strings

## Dependencies
- `<windows.h>` for `MessageBox`, `OutputDebugString`, etc.
- `<cstdio>` for `printf`, `vsnprintf`
- `debug.h` (header) for `DebugLog` declaration
