# Generals/Code/Tools/DebugWindow/DebugWindowExport.h

## Purpose
Header file declaring C-style export functions for a debug window tool in the SAGE engine.

## Responsibilities
- Exposes debug window functionality via C-style exports
- Provides frame control, message logging, and variable inspection
- Supports pausing and fast-forwarding the game
- Manages debug dialog creation/destruction

## Key Types
None

## Key Functions
### CreateDebugDialog
- Purpose: Creates the debug dialog window.
- Calls: None

### DestroyDebugDialog
- Purpose: Destroys the debug dialog and frees resources.
- Calls: None

### CanAppContinue
- Purpose: Checks if the application should continue running.
- Calls: None

### ForceAppContinue
- Purpose: Forces the application to continue (unpauses if needed).
- Calls: None

### RunAppFast
- Purpose: Determines if the app should run in fast-forward mode.
- Calls: None

### AppendMessage
- Purpose: Adds a message to the debug script window.
- Calls: None

### SetFrameNumber
- Purpose: Sets the current frame number for the application.
- Calls: None

### AppendMessageAndPause
- Purpose: Adds a message and pauses the application.
- Calls: None

### AdjustVariable
- Purpose: Updates or sets a variable's value in the debug system.
- Calls: None

### AdjustVariableAndPause
- Purpose: Updates a variable and pauses the application.
- Calls: None

## Globals
None

## Dependencies
- Uses `extern "C"` to prevent name mangling
- Functions marked with `__declspec(dllexport)` for DLL export
