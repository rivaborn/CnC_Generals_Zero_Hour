# GeneralsMD/Code/GameEngine/Source/GameClient/MessageStream/WindowXlat.cpp

## Purpose
Handles translation of raw input messages (mouse/keyboard) into window system events for the game's UI.

## Responsibilities
- Translates raw mouse/keyboard input into game window messages
- Routes input events to the window manager
- Manages input blocking during scrolling or UI disabled states
- Handles special cases like movie escape and placement anchoring

## Key Types
- `WindowTranslator` (Class): Main translator class for input messages
- `GameWindowMessage` (Enum): Window-specific message types (e.g., GWM_LEFT_DOWN)
- `WinInputReturnCode` (Enum): Input processing result codes

## Key Functions
### `rawMouseToWindowMessage`
- Purpose: Converts raw mouse messages to window-specific messages
- Calls: None (pure translation)

### `WindowTranslator::translateGameMessage`
- Purpose: Processes game messages and routes relevant ones to the window system
- Calls: `rawMouseToWindowMessage`, `TheWindowManager->winProcessMouseEvent`, `TheWindowManager->winProcessKey`, `TheDisplay->stopMovie`

## Globals
- `TheWindowManager` (GameWindowManager*): Window system manager instance
- `TheShell` (Shell*): Shell interface instance
- `TheInGameUI` (InGameUI*): In-game UI instance
- `TheDisplay` (Display*): Display system instance
- `TheGlobalData` (GlobalData*): Global game data

## Dependencies
- `Common/MessageStream.h`
- `GameClient/GameWindowManager.h`
- `GameClient/WindowXlat.h`
- `GameClient/Shell.h`
- `GameClient/Display.h`
