# Generals/Code/Tools/ParticleEditor/ParticleEditor.h

## Purpose
Header file for the DEBUGWINDOW DLL, defining the main application class for a debug window tool.

## Responsibilities
- Declares the main application class `CDebugWindowApp` for the debug window tool.
- Manages a dialog window instance via getter/setter methods.
- Provides MFC framework integration for the debug window.
- Includes resource symbols and export definitions.

## Key Types
- `DebugWindowDialog` (Class): Forward declaration of the dialog window class.
- `CDebugWindowApp` (Class): Main application class inheriting from `CWinApp`.

## Key Functions
### `CDebugWindowApp::CDebugWindowApp`
- Purpose: Constructor for the debug window application.
- Calls: None visible.

### `CDebugWindowApp::~CDebugWindowApp`
- Purpose: Destructor for the debug window application.
- Calls: None visible.

### `CDebugWindowApp::GetDialogWindow`
- Purpose: Returns the current dialog window instance.
- Calls: None visible.

### `CDebugWindowApp::SetDialogWindow`
- Purpose: Sets the dialog window instance.
- Calls: None visible.

## Globals
- None.

## Dependencies
- `stdafx.h` (included indirectly)
- `resource.h` (main symbols)
- `ParticleEditorExport.h` (export definitions)
- MFC framework classes (`CWinApp`, `DECLARE_MESSAGE_MAP`)
