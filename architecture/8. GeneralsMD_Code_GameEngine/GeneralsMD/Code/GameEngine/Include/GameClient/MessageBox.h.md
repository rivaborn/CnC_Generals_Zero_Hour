# GeneralsMD/Code/GameEngine/Include/GameClient/MessageBox.h

## Purpose
Header file defining convenience functions for displaying various types of message boxes in the game client.

## Responsibilities
- Declares message box creation functions with different button configurations
- Provides callbacks for user responses
- Integrates with the game window management system

## Key Types
None

## Key Functions
### MessageBoxYesNo
- Purpose: Creates a message box with Yes and No buttons
- Calls: Not inferable

### QuitMessageBoxYesNo
- Purpose: Creates a quit confirmation message box with Yes and No buttons
- Calls: Not inferable

### MessageBoxYesNoCancel
- Purpose: Creates a message box with Yes, No, and Cancel buttons
- Calls: Not inferable

### MessageBoxOkCancel
- Purpose: Creates a message box with Ok and Cancel buttons
- Calls: Not inferable

### MessageBoxOk
- Purpose: Creates a message box with only an Ok button
- Calls: Not inferable

### MessageBoxCancel
- Purpose: Creates a message box with only a Cancel button
- Calls: Not inferable

## Globals
None

## Dependencies
- `GameClient/GameWindowManager.h`
- `UnicodeString` (string type)
- `GameWindow` (window class)
- `GameWinMsgBoxFunc` (callback function type)
