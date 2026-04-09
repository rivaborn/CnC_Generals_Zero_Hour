# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/ExtendedMessageBox.cpp

## Purpose
Implements an extended modal message box system for the game UI, allowing customizable buttons and callbacks.

## Responsibilities
- Creates and manages modal message box windows
- Handles button layout and positioning
- Processes user input via callbacks
- Manages message box lifecycle (creation/destruction)

## Key Types
- `WindowExMessageBoxData` (struct): Stores callback functions and user data for message boxes
- `MessageBoxFunc` (typedef): Callback function type for button actions

## Key Functions
### `gogoExMessageBox`
- Purpose: Creates and configures a message box with specified parameters
- Calls: `TheWindowManager->winCreateFromScript`, `TheWindowManager->winSetModal`, `GadgetStaticTextSetText`, `NEW`

### `ExtendedMessageBoxSystem`
- Purpose: Handles window messages for message boxes (focus, selection, destruction)
- Calls: `delete`, `TheWindowManager->winDestroy`

### `ExMessageBoxYesNo` / `ExMessageBoxYesNoCancel` / `ExMessageBoxOkCancel` / `ExMessageBoxOk` / `ExMessageBoxCancel`
- Purpose: Convenience wrappers for common message box configurations
- Calls: `gogoExMessageBox`

## Globals
- None

## Dependencies
- `GameWindow`, `WindowMsgHandledType`, `UnicodeString` from game engine
- `TheWindowManager`, `TheNameKeyGenerator` global instances
- `GadgetStaticTextSetText` function
- Window layout scripts ("Menus/MessageBox.wnd")
- Message box flag constants (`MSG_BOX_OK`, `MSG_BOX_YES`, etc.)
