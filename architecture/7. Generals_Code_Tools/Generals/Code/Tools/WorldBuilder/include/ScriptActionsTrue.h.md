# Generals/Code/Tools/WorldBuilder/include/ScriptActionsTrue.h

## Purpose
Header for the `ScriptActionsTrue` dialog class used in WorldBuilder for managing script actions.

## Responsibilities
- Manages script action editing UI
- Handles action list operations (add, delete, move, copy)
- Provides data exchange for dialog controls
- Maintains references to script and current action

## Key Types
- **ScriptActionsTrue (Class)**: Dialog for editing script actions
- **Script (Class)**: Reference to the script being edited
- **ScriptAction (Class)**: Currently selected action
- **SidesList (Class)**: Used for side management
- **IDD (Enum)**: Dialog resource ID

## Key Functions
### DoDataExchange
- Purpose: Handles DDX/DDV for dialog data exchange
- Calls: Not inferable

### setScript
- Purpose: Sets the script reference
- Calls: None

### enableUI
- Purpose: Enables/disables UI controls based on selection
- Calls: Not inferable

### loadList
- Purpose: Loads the list of script actions into the UI
- Calls: Not inferable

### doMoveDown
- Purpose: Moves the selected action down in the list
- Calls: Not inferable

### OnInitDialog
- Purpose: Initializes the dialog
- Calls: enableUI, loadList

### OnEditAction
- Purpose: Handles editing of the selected action
- Calls: Not inferable

### OnSelchangeActionList
- Purpose: Handles selection changes in the action list
- Calls: enableUI

### OnDblclkActionList
- Purpose: Handles double-click on action list
- Calls: Not inferable

### OnNew
- Purpose: Creates a new action
- Calls: Not inferable

### OnDelete
