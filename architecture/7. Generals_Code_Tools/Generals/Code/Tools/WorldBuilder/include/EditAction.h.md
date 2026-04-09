# Generals/Code/Tools/WorldBuilder/include/EditAction.h

## Purpose
Header file for the `EditAction` dialog class used in WorldBuilder to edit script actions.

## Responsibilities
- Manages UI for editing script actions
- Handles data exchange between dialog controls and script action data
- Formats script action text for display
- Provides timer-based updates for the dialog

## Key Types
- **ScriptAction (Class)**: Reference to script action being edited
- **SidesList (Class)**: Reference to sides list (forward declaration)
- **EditAction (Class)**: Dialog class for editing script actions
- **(anonymous enum) (Enum)**: Contains IDD_ScriptAction dialog ID
- **IDD (Enum)**: Dialog resource ID

## Key Functions
### EditAction::DoDataExchange
- Purpose: Handles DDX/DDV data exchange for dialog controls
- Calls: Not inferable

### EditAction::OnNotify
- Purpose: Processes Windows notifications for the dialog
- Calls: Not inferable

### EditAction::setAction
- Purpose: Sets the script action being edited
- Calls: Not inferable

### EditAction::formatScriptActionText
- Purpose: Formats script action text for display in the rich edit control
- Calls: Not inferable

### EditAction::OnInitDialog
- Purpose: Initializes dialog controls when the dialog is created
- Calls: Not inferable

### EditAction::OnSelchangeScriptActionType
- Purpose: Handles changes to the script action type selection
- Calls: Not inferable

### EditAction::OnTimer
- Purpose: Handles timer events for the dialog
- Calls: Not inferable

## Globals
- **m_action (ScriptAction*)**: Pointer to the script action being edited
- **m_updating (Bool)**: Flag indicating if the dialog is updating
- **m_mod
