# GeneralsMD/Code/GameEngine/Include/GameClient/GameWindowManager.h

## Purpose
Header defining the `GameWindowManager` class, which manages the game's windowing system for menus and GUI controls.

## Responsibilities
- Manages creation, destruction, and updating of game windows
- Handles input processing (mouse/keyboard) for windows
- Provides default drawing and system functions for UI elements
- Maintains window hierarchy and focus management

## Key Types
- `GameWindow` (Class): Base class for game windows
- `WindowLayoutInfo` (Class): Contains layout metadata (version, callbacks, etc.)
- `GameWindowManager` (Class): Singleton manager for window system
- `GameWindowList` (typedef): List of `GameWindow*` pointers

## Key Functions
### `winCreateFromScript`
- Purpose: Creates new window(s) from a .wnd script file
- Calls: Not inferable

### `winProcessMouseEvent`
- Purpose: Processes a single mouse event
- Calls: Not inferable

### `winProcessKey`
- Purpose: Processes a single key event
- Calls: Not inferable

### `winDrawImage`
- Purpose: Draws an image at specified screen coordinates
- Calls: Not inferable

## Globals
- `TheWindowManager` (GameWindowManager*): Singleton instance of the window manager
- `WindowLayoutCurrentVersion` (UnsignedInt): Current version of window layouts

## Dependencies
- `Common/STLTypedefs.h`, `Common/SubsystemInterface.h`
- `GameClient/WindowLayout.h`, `GameClient/KeyDefs.h`, `GameClient/Gadget.h`
- `GameWinDrawFunc`, `GameWinSystemFunc`, `GameWinInputFunc`, etc. (function pointers)
