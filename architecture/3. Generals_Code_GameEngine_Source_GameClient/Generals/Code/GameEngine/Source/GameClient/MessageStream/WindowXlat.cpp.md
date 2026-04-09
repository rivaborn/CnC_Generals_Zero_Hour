# Generals/Code/GameEngine/Source/GameClient/MessageStream/WindowXlat.cpp

## Purpose
Handles translation of raw input messages (mouse/keyboard) into window system-specific messages for the game's UI.

## Responsibilities
- Translates raw mouse/keyboard events into game window messages
- Routes input to the window manager or shell based on game state
- Manages input consumption (destroying or keeping messages)
- Handles special cases like movie escape and UI input locking

## Key Types
- `WindowTranslator` (Class): Main translator class that processes input messages
- `GameWindowMessage` (Enum): Window-specific message types (e.g., GWM_LEFT_DOWN)
- `WinInputReturnCode` (Enum): Input processing result codes

## Key Functions
### `rawMouseToWindowMessage`
- Purpose: Converts raw mouse messages to window-specific messages
- Calls: None (pure translation logic)

### `WindowTranslator::translateGameMessage`
- Purpose: Processes game messages and routes them to appropriate handlers
- Calls: `rawMouseToWindowMessage`, `TheWindowManager->winProcessMouseEvent`, `TheWindowManager->winProcessKey`, `TheDisplay->stopMovie`

## Globals
- `TheMousePos` (ICoord2D): Debug-only mouse position tracking
- `TheTacticalView`, `TheWindowManager`, `TheShell`, `TheInGameUI`, `TheDisplay`, `TheGlobalData`: Game system globals

## Dependencies
- `MessageStream.h`, `GameWindowManager.h`, `WindowXlat.h`, `Shell.h`, `Display.h`
- `GameMessage`, `ICoord2D`, `GameWindowMessage`, `WinInputReturnCode` types
