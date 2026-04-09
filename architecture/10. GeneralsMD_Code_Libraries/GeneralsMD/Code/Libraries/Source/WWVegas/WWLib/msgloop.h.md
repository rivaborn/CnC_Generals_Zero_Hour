# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/msgloop.h

## Purpose
Header file defining the Windows message loop handling interface for the SAGE engine.

## Responsibilities
- Declares the main Windows message handler function
- Provides modeless dialog box management functions
- Declares accelerator key support functions
- Defines a general-purpose message intercept handler callback

## Key Types
None

## Key Functions
### Windows_Message_Handler
- Purpose: Main message handler for Windows messages
- Calls: Not inferable

### Remove_Modeless_Dialog
- Purpose: Removes a modeless dialog from the message loop
- Calls: Not inferable

### Add_Modeless_Dialog
- Purpose: Adds a modeless dialog to the message loop
- Calls: Not inferable

### Add_Accelerator
- Purpose: Adds an accelerator table to a window
- Calls: Not inferable

### Remove_Accelerator
- Purpose: Removes an accelerator table
- Calls: Not inferable

## Globals
- Message_Intercept_Handler (bool (*)(MSG &)): Callback for intercepting Windows messages

## Dependencies
- `<windows.h>`: For Windows API types and constants
