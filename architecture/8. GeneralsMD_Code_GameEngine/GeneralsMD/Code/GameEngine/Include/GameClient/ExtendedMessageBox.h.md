# GeneralsMD/Code/GameEngine/Include/GameClient/ExtendedMessageBox.h

## Purpose
Defines an extended message box system for the game client, supporting various button configurations and callbacks.

## Responsibilities
- Declares message box return types and callback function pointers
- Defines data structure for message box window data
- Provides function declarations for creating different types of message boxes (Yes/No, Yes/No/Cancel, Ok/Cancel, Ok, Cancel)

## Key Types
- MessageBoxReturnType (Enum): return codes for message box callbacks (MB_RETURN_CLOSE, MB_RETURN_KEEPOPEN)
- MessageBoxFunc (Function pointer): callback function type for message box buttons
- WindowExMessageBoxData (Struct): data attached to each extended message box window, containing callback functions and user data

## Key Functions
### ExMessageBoxYesNo
- Purpose: Creates a Yes/No message box with specified title, body, user data, and callbacks
- Calls: Not inferable (declaration only)

### ExMessageBoxYesNoCancel
- Purpose: Creates a Yes/No/Cancel message box with specified title, body, user data, and callbacks
- Calls: Not inferable (declaration only)

### ExMessageBoxOkCancel
- Purpose: Creates an Ok/Cancel message box with specified title, body, user data, and callbacks
- Calls: Not inferable (declaration only)

### ExMessageBoxOk
- Purpose: Creates an Ok-only message box with specified title, body, user data, and callback
- Calls: Not inferable (declaration only)

### ExMessageBoxCancel
- Purpose: Creates a Cancel-only message box with specified title, body, user data, and callback
- Calls: Not inferable (declaration only)

## Globals
None

## Dependencies
- GameClient/GameWindowManager.h (included)
