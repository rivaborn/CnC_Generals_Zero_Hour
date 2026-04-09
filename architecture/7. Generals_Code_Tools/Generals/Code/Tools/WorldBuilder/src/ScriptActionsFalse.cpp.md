# Generals/Code/Tools/WorldBuilder/src/ScriptActionsFalse.cpp

## Purpose
Implements a property page for editing false-action scripts in the WorldBuilder tool.

## Responsibilities
- Manages UI for false-action script editing
- Handles action creation, deletion, copying, and reordering
- Updates script comments and validates actions
- Synchronizes UI with script data

## Key Types
- ScriptActionsFalse (CPropertyPage): Property page class for false-action editing
- ScriptAction*: Pointer to script actions in the false-action chain

## Key Functions
### ScriptActionsFalse::OnInitDialog
- Purpose: Initializes the dialog and loads the action list
- Calls: CPropertyPage::OnInitDialog, ScriptDialog::updateScriptWarning, loadList

### ScriptActionsFalse::loadList
- Purpose: Populates the list box with false actions
- Calls: ScriptDialog::updateScriptWarning, CListBox methods

### ScriptActionsFalse::OnEditAction
- Purpose: Opens the edit dialog for the selected action
- Calls: EditAction::DoModal, ScriptDialog::updateScriptWarning, CListBox methods

### ScriptActionsFalse::enableUI
- Purpose: Enables/disables UI controls based on selection
- Calls: CWnd::EnableWindow

### ScriptActionsFalse::OnSelchangeActionList
- Purpose: Handles list selection changes and updates UI state
- Calls: enableUI

### ScriptActionsFalse::OnNew
- Purpose: Creates a new action in the false-action chain
- Calls: newInstance, EditAction::DoModal, loadList

### ScriptActionsFalse::OnDelete
- Purpose: Removes the selected action from the chain
- Calls: Script::deleteFalseAction, loadList

### ScriptActionsFalse::OnCopy
- Purpose: Duplicates the selected action
- Calls: ScriptAction::duplicate, loadList

### ScriptActionsFalse::doMoveDown
- Purpose: Moves the selected action down in the chain
- Calls: ScriptAction methods (setNextAction)

### ScriptActionsFalse::OnMoveUp
- Purpose: Moves the selected action up in the chain
- Calls: doMoveDown, loadList

### ScriptActionsFalse::OnChangeEditComment
- Purpose: Updates the script comment from the UI
- Calls: Script::setActionComment

## Globals
- None

## Dependencies
- "stdafx.h", "worldbuilder.h", "ScriptActionsFalse.h", "GameLogic/Scripts.h", "EditAction.h", "ScriptDialog.h"
- CPropertyPage, CListBox, CWnd, CString, AsciiString, Script, ScriptAction, EditAction, ScriptDialog classes
