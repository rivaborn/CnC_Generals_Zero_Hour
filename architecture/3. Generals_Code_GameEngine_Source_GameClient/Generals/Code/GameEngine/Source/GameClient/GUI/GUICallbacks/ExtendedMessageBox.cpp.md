# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/ExtendedMessageBox.cpp

## Purpose
Implements extended modal message boxes for the game UI, supporting various button configurations and callbacks.

## Responsibilities
- Creates and manages message box windows with customizable buttons and text
- Handles button click events and executes associated callbacks
- Manages window focus and destruction
- Supports different message box types (Yes/No, OK/Cancel, etc.)

## Key Types
- `WindowExMessageBoxData` (struct): Stores callback functions and user data for message boxes
- `MessageBoxFunc` (typedef): Function pointer type for message box callbacks

## Key Functions
### `gogoExMessageBox`
- Purpose: Creates and configures a message box window with specified parameters
- Calls: `TheWindowManager->winCreateFromScript`, `TheWindowManager->winSetModal`, `GadgetStaticTextSetText`, `NEW`

### `ExtendedMessageBoxSystem`
- Purpose: Handles window messages for message boxes (focus, destruction, button clicks)
- Calls: `delete`, `TheWindowManager->winDestroy`, callback functions from `WindowExMessageBoxData`

### `ExMessageBoxYesNo`, `ExMessageBoxYesNoCancel`, `ExMessageBoxOkCancel`, `ExMessageBoxOk`, `ExMessageBoxCancel`
- Purpose: Convenience functions for creating specific message box types
- Calls: `gogoExMessageBox`

## Globals
- None

## Dependencies
- `PreRTS.h`, `GameEngine.h`, `NameKeyGenerator.h`, `WindowLayout.h`, `Gadget.h`, `Shell.h`, `KeyDefs.h`, `GadgetStaticText.h`, `GameWindowManager.h`, `ExtendedMessageBox.h`
- `TheWindowManager`, `TheNameKeyGenerator` (global instances)
- `WindowMsgHandledType`, `GameWindow`, `UnicodeString`, `MessageBoxFunc` (external types)
