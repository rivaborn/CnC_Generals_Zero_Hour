# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/MessageBox.cpp

## Purpose
Handles message box UI creation and event callbacks for user confirmation dialogs.

## Responsibilities
- Creates message boxes with various button configurations (Yes/No, Ok/Cancel, etc.)
- Manages button click callbacks
- Handles window focus and destruction events
- Differentiates between regular and quit-style message boxes

## Key Types
- `WindowMessageBoxData` (struct): Stores callback functions for message box buttons

## Key Functions
### MessageBoxYesNo
- Purpose: Creates a Yes/No message box
- Calls: `TheWindowManager->gogoMessageBox`

### MessageBoxYesNoCancel
- Purpose: Creates a Yes/No/Cancel message box
- Calls: `TheWindowManager->gogoMessageBox`

### MessageBoxOkCancel
- Purpose: Creates an Ok/Cancel message box
- Calls: `TheWindowManager->gogoMessageBox`

### MessageBoxOk
- Purpose: Creates an Ok-only message box
- Calls: `TheWindowManager->gogoMessageBox`

### MessageBoxCancel
- Purpose: Creates a Cancel-only message box
- Calls: `TheWindowManager->gogoMessageBox`

### MessageBoxSystem
- Purpose: Handles window messages for regular message boxes
- Calls: `TheWindowManager->winDestroy`, `TheNameKeyGenerator->nameToKey`

### QuitMessageBoxSystem
- Purpose: Handles window messages for quit-style message boxes
- Calls: `TheWindowManager->winDestroy`, `TheNameKeyGenerator->nameToKey`

## Globals
- None

## Dependencies
- `GameEngine.h`, `NameKeyGenerator.h`, `WindowLayout.h`, `Gadget.h`, `Shell.h`, `KeyDefs.h`, `GameWindowManager.h`, `MessageBox.h`
- `TheWindowManager`, `TheNameKeyGenerator`
