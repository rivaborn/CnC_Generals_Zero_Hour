# Generals/Code/Tools/WW3D/max2w3d/floaterdialog.h

## Purpose
Defines a class for creating and managing modeless dialog boxes in the Max2W3D tool.

## Responsibilities
- Manages creation and lifecycle of modeless dialog windows
- Handles dialog procedure callbacks
- Tracks child dialog template IDs and procedures
- Provides interface for checking dialog creation status

## Key Types
- **FloaterDialogClass (Class)**: Manages modeless dialog boxes in the Max2W3D tool
- **Interface (Class)**: External interface type used for dialog creation

## Key Functions
### FloaterDialogClass::Create
- Purpose: Creates a modeless dialog box with specified child dialog template and procedure
- Calls: Not inferable (implementation in .cpp)

### FloaterDialogClass::Dialog_Proc
- Purpose: Handles Windows messages for the dialog box
- Calls: Not inferable (implementation in .cpp)

## Globals
- None

## Dependencies
- `<windows.h>` for Windows API types (HWND, DLGPROC, etc.)
- `Interface` class (forward declared)
