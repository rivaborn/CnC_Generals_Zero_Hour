# Generals/Code/Tools/WorldBuilder/include/ScriptActionsFalse.h

## Purpose
Header for a property page dialog class (`ScriptActionsFalse`) used in the WorldBuilder tool to manage script actions.

## Responsibilities
- Manages UI for editing script actions
- Handles action selection, creation, deletion, and reordering
- Provides methods for enabling/disabling UI controls
- Loads and displays script action lists

## Key Types
- **ScriptActionsFalse (Class)**: Property page for managing script actions.
- **Script (Class)**: Reference to the script being edited.
- **ScriptAction (Class)**: Currently selected action.
- **SidesList (Class)**: Not used in this file.
- **IDD (Enum)**: Dialog resource ID.

## Key Functions
### `DoDataExchange`
- Purpose: Handles data exchange between UI controls and member variables.
- Calls: `CPropertyPage::DoDataExchange`

### `setScript`
- Purpose: Sets the script reference for this dialog.
- Calls: None

### `enableUI`
- Purpose: Enables/disables UI controls based on selection state.
- Calls: None

### `loadList`
- Purpose: Loads the list of script actions into the UI.
- Calls: None

### `doMoveDown`
- Purpose: Moves the selected action down in the list.
- Calls: None

### `OnInitDialog`
- Purpose: Initializes the dialog when created.
- Calls: `enableUI`, `loadList`

### `OnEditAction`
- Purpose: Handles editing the currently selected action.
- Calls: None

### `OnSelchangeActionList`
- Purpose: Handles selection changes in the action list.
- Calls: `enableUI`

### `OnDblclkActionList`
- Purpose: Handles double-click events on the action list.
- Calls: None

### `
