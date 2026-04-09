# Generals/Code/Tools/WorldBuilder/src/ScriptActionsTrue.cpp

## Purpose
Implements the `ScriptActionsTrue` property page for the WorldBuilder tool, managing script actions in the UI.

## Responsibilities
- Handles UI events for script action management (edit, delete, copy, move).
- Maintains a list of script actions and their order.
- Updates the UI based on the current script action selection.
- Interfaces with `ScriptAction` objects and the `ScriptDialog` for validation.

## Key Types
- **ScriptActionsTrue (CPropertyPage)**: Property page for managing script actions.
- **ScriptAction**: Represents individual script actions (external).
- **ScriptDialog**: Manages script validation (external).

## Key Functions
### `OnInitDialog`
- Purpose: Initializes the dialog and loads the action list.
- Calls: `ScriptDialog::updateScriptWarning`, `loadList`.

### `loadList`
- Purpose: Populates the list box with script actions.
- Calls: `ScriptAction::getUiText`, `ScriptAction::getNext`.

### `OnEditAction`
- Purpose: Opens the edit dialog for the selected action.
- Calls: `EditAction::DoModal`, `ScriptDialog::updateScriptWarning`.

### `enableUI`
- Purpose: Enables/disables UI controls based on the current selection.
- Calls: None.

### `OnNew`
- Purpose: Creates a new script action.
- Calls: `newInstance`, `EditAction::DoModal`, `loadList`.

### `OnDelete`
- Purpose: Deletes the selected script action.
- Calls: `Script::deleteAction`, `loadList`.

### `OnCopy`
- Purpose: Copies the selected script action.
- Calls: `ScriptAction::duplicate`, `loadList`.

### `doMoveDown`
- Purpose: Moves the selected action down in the list.
- Calls: `ScriptAction::getNext`, `ScriptAction::setNextAction`.

### `OnMoveUp`
- Purpose: Moves the selected action up in the list.
- Calls: `doMoveDown`, `loadList`.

### `OnChangeEditComment`
- Purpose: Updates the script comment.
- Calls: None.

## Globals
- **m_action (ScriptAction*)**: Current selected action.
- **m_index (Int)**: Index of the current action in the list.
- **m_script (Script*)**: The script being edited (external).

## Dependencies
- `stdafx.h`, `worldbuilder.h`, `ScriptActionsTrue.h`, `GameLogic/Scripts.h`, `EditAction.h`, `ScriptDialog.h`.
- `CPropertyPage`, `CListBox`, `CWnd`, `CString`, `AsciiString`, `ScriptAction`, `Script`, `EditAction`.
