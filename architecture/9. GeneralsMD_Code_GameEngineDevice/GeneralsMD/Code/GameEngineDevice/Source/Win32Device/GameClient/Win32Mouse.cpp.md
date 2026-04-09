# GeneralsMD/Code/GameEngineDevice/Source/Win32Device/GameClient/Win32Mouse.cpp

## Purpose
Handles Win32-specific mouse input and cursor management for the game.

## Responsibilities
- Translates Win32 mouse messages into internal game events
- Manages mouse cursor visibility and type
- Buffers mouse input events for processing
- Loads cursor resources from files

## Key Types
- `Win32Mouse` (Class): Win32 mouse input handler
- `MouseIO` (Struct): Mouse input event data
- `MouseCursor` (Enum): Mouse cursor types

## Key Functions
### `getMouseEvent`
- Purpose: Retrieves a mouse event from the input buffer
- Calls: `translateEvent`

### `translateEvent`
- Purpose: Converts Win32 mouse messages to internal format
- Calls: `TheGameClient->getFrame()`

### `addWin32Event`
- Purpose: Stores Win32 mouse messages in the input buffer
- Calls: None

### `setCursor`
- Purpose: Changes the visible mouse cursor
- Calls: `SetCursor`

### `initCursorResources`
- Purpose: Preloads cursor resources from files
- Calls: `LoadCursorFromFile`

## Globals
- `TheWin32Mouse` (Win32Mouse*): Global mouse handler instance
- `cursorResources` (HCURSOR[]): Array of loaded cursor resources
- `ApplicationHInstance` (HINSTANCE): Global application instance handle

## Dependencies
- `windows.h` for Win32 API
- `Win32Mouse.h` for class definition
- `GameClient.h` for game client interface
- `WinMain.h` for application handle
