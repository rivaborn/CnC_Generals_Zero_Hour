# Generals/Code/GameEngine/Source/Common/System/Debug.cpp

## Purpose
This file contains debug logging and utility functions for the Command & Conquer Generals game engine, including crash handling, message boxes, and stack trace generation.

## Responsibilities
- Handle debug initialization and shutdown.
- Log messages to console and/or log files.
- Present assertion failure dialogs.
- Generate and log stack traces.
- Manage crash reporting in release builds.

## Key Types
- None

## Key Functions
### getCurrentTimeString
- Purpose: Returns the current time as a string.
- Calls: `time`, `localtime`, `asctime`

### getCurrentTickString
- Purpose: Returns the current tick count as a string.
- Calls: `GetTickCount`

### prepBuffer
- Purpose: Prepares a buffer by optionally adding a timestamp.
- Calls: `getCurrentTimeString`, `strcpy`, `strcat`

### doCrashBox
- Purpose: Presents an assertion failure message box and handles user input.
- Calls: `MessageBoxWrapper`, `_exit`, `DebugBreak`

### whackFunnyCharacters
- Purpose: Replaces non-printable characters in a string with spaces.
- Calls: None

### ReleaseCrash
- Purpose: Handles critical errors by logging details and displaying an error message box.
- Calls: `remove`, `rename`, `fopen`, `fprintf`, `fflush`, `fclose`, `MessageBox`

## Globals
- DX8Wrapper_IsWindowed (bool): Indicates if the application is running in windowed mode.
- ApplicationHWnd (HWND): Handle to the main application window.
- gAppPrefix (char*): Prefix for log file names.
- theBuffer (char[8192]): Buffer used for formatting debug messages.
- theDebugFlags (int): Flags controlling debug behavior.
- theMainThreadID (DWORD): ID of the main thread.
- TheCurrentIgnoreCrashPtr (char*): Pointer to a flag indicating if crashes should be ignored.

## Dependencies
- Key includes: `PreRTS.h`, `Common/CriticalSection.h`, `Common/Debug.h`, `Common/registry.h`, `Common/SystemInfo.h`, `Common/UnicodeString.h`, `GameClient/GameText.h`, `GameClient/Keyboard.h`, `GameClient/Mouse.h`, `Common/StackDump.h`
- External symbols: `DX8Wrapper_IsWindowed`, `ApplicationHWnd`, `gAppPrefix`, `TheGlobalData`, `TheKeyboard`, `TheMouse`, `GetRegistryLanguage`, `TheGameText`, `TheSystemIsUnicode`
