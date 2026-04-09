# Generals/Code/Tools/DebugWindow/DebugWindow.h

## Purpose
Header file for the DEBUGWINDOW DLL, defining the main application class for a debug window tool.

## Responsibilities
- Declares the main application class `CDebugWindowApp` for the debug window tool.
- Manages the debug window dialog instance.
- Provides accessor methods for the dialog window.
- Defines message map for MFC message handling.

## Key Types
- **CDebugWindowApp (Class)**: Main application class for the debug window tool.
- **DebugWindowDialog (Class)**: Forward-declared dialog class used by the application.

## Key Functions
### CDebugWindowApp()
- Purpose: Constructor for the debug window application.
- Calls: None

### ~CDebugWindowApp()
- Purpose: Destructor for the debug window application.
- Calls: None

### GetDialogWindow()
- Purpose: Returns the current dialog window instance.
- Calls: None

### SetDialogWindow()
- Purpose: Sets the dialog window instance.
- Calls: None

### DECLARE_MESSAGE_MAP()
- Purpose: Declares the message map for MFC message handling.
- Calls: None

## Globals
- **m_DialogWindow (DebugWindowDialog*)**: Stores the pointer to the debug window dialog instance.

## Dependencies
- `resource.h`: Main symbols for the application.
- `DebugWindowExport.h`: Export definitions for the DLL.
- MFC classes (`CWinApp`).
- Windows SDK headers (included via `stdafx.h`).
