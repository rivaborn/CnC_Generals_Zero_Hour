# Generals/Code/GameEngineDevice/Source/Win32Device/Common/Win32OSDisplay.cpp

## Purpose
Handles Windows-specific OS display functionality, including message boxes and flag conversions.

## Responsibilities
- Converts game-specific dialog flags to Windows MessageBox flags
- Displays modal warning dialogs with localized text
- Manages Unicode/ANSI string handling for message boxes
- Ensures proper window positioning during dialog display

## Key Types
- None

## Key Functions
### RTSFlagsToOSFlags
- Purpose: Converts game-specific dialog flags to Windows MessageBox flags
- Calls: BitTest

### OSDisplayWarningBox
- Purpose: Displays a localized warning message box and returns user response
- Calls: RTSFlagsToOSFlags, TheGameText->fetch, UnicodeString::translate, SetWindowPos, MessageBoxW, MessageBoxA

## Globals
- ApplicationHWnd (HWND): Stores the main application window handle

## Dependencies
- windows.h
- Common/OSDisplay.h
- Common/SubsystemInterface.h
- Common/STLTypeDefs.h
- Common/AsciiString.h
- Common/SystemInfo.h
- Common/UnicodeString.h
- GameClient/GameText.h
- TheGameText (GameText*)
- TheSystemIsUnicode (bool)
