# Generals/Code/Tools/WorldBuilder/include/EditGroup.h

## Purpose
Header file for the `EditGroup` dialog class used in WorldBuilder to edit script groups.

## Responsibilities
- Defines the `EditGroup` dialog class for editing `ScriptGroup` objects.
- Manages data exchange between UI controls and the `ScriptGroup` instance.
- Handles dialog initialization and OK button click events.
- Declares message map for MFC dialog handling.

## Key Types
- **ScriptGroup (Class)**: Reference to the script group being edited.
- **EditGroup (Class)**: MFC dialog class for editing script groups.
- **(anonymous enum) (Enum)**: Contains `IDD` enum value for dialog resource ID.
- **IDD (Enum)**: Dialog resource identifier.

## Key Functions
### EditGroup::EditGroup
- Purpose: Constructor for the `EditGroup` dialog.
- Calls: None visible.

### EditGroup::DoDataExchange
- Purpose: Handles data exchange between dialog controls and member variables.
- Calls: `CDataExchange` methods.

### EditGroup::OnOK
- Purpose: Handles the OK button click event.
- Calls: Not inferable.

### EditGroup::OnInitDialog
- Purpose: Initializes the dialog when it is created.
- Calls: Not inferable.

### DECLARE_MESSAGE_MAP
- Purpose: Declares the message map for the dialog class.
- Calls: Not inferable.

## Globals
- **m_scriptGroup (ScriptGroup*)**: Pointer to the script group being edited.

## Dependencies
- `CDialog`, `CWnd`, `CDataExchange` (MFC classes).
- `ScriptGroup` (forward-declared class).
- `DECLARE_MESSAGE_MAP()` (MFC macro).
