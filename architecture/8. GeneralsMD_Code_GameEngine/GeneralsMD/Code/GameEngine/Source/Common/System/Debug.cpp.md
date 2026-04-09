# GeneralsMD/Code/GameEngine/Source/Common/System/Debug.cpp

## Purpose
Provides debug logging, crash handling, and profiling utilities for the game engine.

## Responsibilities
- Manages debug log file I/O and console output
- Handles assertion failures with user dialogs
- Provides stack trace dumps for crashes
- Implements release-mode crash reporting
- Offers simple profiling functionality

## Key Types
- **SimpleProfiler (Class)**: High-resolution timer for performance measurement
- **None**: No other significant structs/classes/enums

## Key Functions
### DebugInit
- Purpose: Initializes debug system with specified flags
- Calls: `GetCurrentThreadId()`, `GetModuleFileName()`, `remove()`, `rename()`, `fopen()`

### DebugLog
- Purpose: Logs formatted messages to file/console
- Calls: `prepBuffer()`, `vsprintf()`, `whackFunnyCharacters()`, `doLogOutput()`

### DebugCrash
- Purpose: Displays crash dialog and logs assertion failures
- Calls: `prepBuffer()`, `vsprintf()`, `whackFunnyCharacters()`, `doLogOutput()`, `doStackDump()`, `doCrashBox()`

### ReleaseCrash
- Purpose: Handles fatal errors in release builds
- Calls: `getCurrentTimeString()`, `FillStackAddresses()`, `StackDumpFromAddresses()`, `MessageBox()`

### ReleaseCrashLocalized
- Purpose: Localized version of ReleaseCrash
- Calls: `fetch()`, `translate()`, `MessageBoxW()`, `MessageBoxA()`

## Globals
- **DX8Wrapper_IsWindowed (bool)**: Tracks windowed mode state
- **ApplicationHWnd (HWND)**: Main application window handle
- **gAppPrefix (char*)**: Prefix for log file names
- **theBuffer (char[])**: Buffer for debug messages
- **theDebugFlags (int)**: Current debug system flags
- **theMainThreadID (DWORD)**: ID of main thread
- **TheCurrentIgnoreCrashPtr (char*)**: Pointer for crash ignore state
- **theReleaseCrashLogFile (FILE*)**: File handle for release crash logs

## Dependencies
- `PreRTS.h`, `Debug.h`, `SystemInfo.h`, `UnicodeString.h`, `GameText.h`, `Keyboard.h`, `Mouse.h`
- `CriticalSection.h` (for thread safety)
- `StackDump.h` (for stack traces)
- Windows API (`MessageBox`, `GetTickCount`, etc.)
- Standard C runtime (`fopen`, `fprintf`, etc.)
