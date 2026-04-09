# Generals/Code/Libraries/Source/WWVegas/WWLib/mono.cpp

## Purpose
Implements monochrome text display functionality for the game, primarily for legacy DOS/Windows text output.

## Responsibilities
- Manages monochrome screen objects and their display
- Provides text rendering, formatting, and positioning
- Handles screen scrolling, clearing, and attribute manipulation
- Supports sub-windows and cursor control

## Key Types
- MonoClass (Class): Main monochrome display class handling text output and screen management
- MonoAttribute (Type): Text attribute enum (not shown in code but referenced)

## Key Functions
### MonoClass::Printf
- Purpose: Prints formatted text to monochrome screen
- Calls: Print, vsprintf, Fetch_String

### MonoClass::Text_Print
- Purpose: Prints text at specified coordinates with attributes
- Calls: Set_Cursor, Print

### MonoClass::Clear
- Purpose: Clears the monochrome screen
- Calls: DeviceIoControl

### MonoClass::Scroll
- Purpose: Scrolls the monochrome screen
- Calls: DeviceIoControl

### MonoClass::View
- Purpose: Brings the mono object to the main display
- Calls: DeviceIoControl

## Globals
- Enabled (bool): Flag indicating if mono output is enabled
- Current (MonoClass*): Pointer to currently displayed mono screen

## Dependencies
- "always.h", "data.h", "mono.h", "monodrvr.h", "stdio.h"
- Windows API: CreateFile, CloseHandle, DeviceIoControl, WriteFile
- External function: Fetch_String (not defined here)
