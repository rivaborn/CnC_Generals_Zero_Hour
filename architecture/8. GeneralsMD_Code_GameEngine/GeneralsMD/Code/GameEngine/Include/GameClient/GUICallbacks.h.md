# GeneralsMD/Code/GameEngine/Include/GameClient/GUICallbacks.h

## Purpose
Header file declaring GUI callback functions for the Command & Conquer Generals game.

## Responsibilities
- Declares callback functions for various UI menus and windows
- Defines enum for in-game chat types
- Provides interface for game window message handling

## Key Types
- InGameChatType (Enum): defines chat scope (allies/everyone/players)

## Key Functions
### MainMenuInit/Update/Shutdown/System/Input
- Purpose: Main menu lifecycle and message handling
- Calls: Not inferable

### SinglePlayerMenuInit/Update/Shutdown/System/Input
- Purpose: Single player menu lifecycle and message handling
- Calls: Not inferable

### OptionsMenuInit/Update/Shutdown/System/Input
- Purpose: Options menu lifecycle and message handling
- Calls: Not inferable

### ControlBarSystem/Input
- Purpose: Handles control bar system messages and input
- Calls: Not inferable

### InGameChatSystem/Input
- Purpose: Manages in-game chat functionality
- Calls: Not inferable

### ToggleControlBar/HideControlBar/ShowControlBar
- Purpose: Controls visibility of control bar
- Calls: Not inferable

### ToggleInGameChat/HideInGameChat/ShowInGameChat
- Purpose: Controls visibility of in-game chat
- Calls: Not inferable

## Globals
None

## Dependencies
- GameClient/GameWindow.h
- WindowLayout, WindowMsgHandledType, GameWindow, UnsignedInt, WindowMsgData, Bool, WinInstanceData types
