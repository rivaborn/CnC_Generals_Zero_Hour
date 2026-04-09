# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/MessageBox.cpp

## Purpose
Implements message box UI controls for the game, handling user input and callbacks.

## Responsibilities
- Creates message boxes with various button configurations (Yes/No, Ok/Cancel, etc.)
- Manages message box lifecycle (creation, input handling, destruction)
- Executes callbacks when buttons are clicked
- Handles focus and input events for message boxes

## Key Types
- `WindowMessageBoxData` (struct): Stores callback functions for message box buttons

## Key Functions
### `MessageBoxYesNo`
- Purpose: Creates a Yes/No message box.
- Calls: `TheWindowManager->gogoMessageBox`

### `QuitMessageBoxYesNo`
- Purpose: Creates a Yes/No message box that may trigger game quit.
- Calls: `TheWindowManager->gogoMessageBox`

### `MessageBoxYesNoCancel`
- Purpose: Creates a Yes/No/Cancel message box.
- Calls: `TheWindowManager->gogoMessageBox`

### `MessageBoxOkCancel`
- Purpose: Creates an Ok/Cancel message box.
- Calls: `TheWindowManager->gogoMessageBox`

### `MessageBoxOk`
- Purpose: Creates an Ok-only message box.
- Calls: `TheWindowManager->gogoMessageBox`

### `MessageBoxCancel`
- Purpose: Creates a Cancel-only message box.
- Calls: `TheWindowManager->gogoMessageBox`

### `MessageBoxSystem`
- Purpose: Handles system messages for standard message boxes.
- Calls: `TheNameKeyGenerator->nameToKey`, `TheWindowManager->winDestroy`

### `QuitMessageBoxSystem`
- Purpose: Handles system messages for quit message boxes.
- Calls: `TheNameKeyGenerator->nameToKey`, `TheWindowManager->winDestroy`

## Globals
- `TheWindowManager` (GameWindowManager*): Manages game windows
- `TheNameKeyGenerator` (NameKeyGenerator*): Converts names to keys

## Dependencies
- `PreRTS.h`, `GameEngine.h`, `NameKeyGenerator.h`, `WindowLayout.h`, `Gadget.h`, `Shell.h`, `KeyDefs.h`, `GameWindowManager.h`, `MessageBox.h`
