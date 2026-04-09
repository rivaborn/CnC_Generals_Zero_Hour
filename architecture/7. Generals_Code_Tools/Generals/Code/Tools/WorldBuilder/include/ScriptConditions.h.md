# Generals/Code/Tools/WorldBuilder/include/ScriptConditions.h

## Purpose
Header file for the ScriptConditionsDlg class, which manages script conditions in the WorldBuilder tool.

## Responsibilities
- Defines the ScriptConditionsDlg dialog class for editing script conditions
- Declares methods for manipulating OR conditions and individual conditions
- Manages UI state and data exchange for the dialog

## Key Types
- ScriptConditionsDlg (Class): Dialog for editing script conditions
- Script (Class): Reference to the script being edited
- OrCondition (Class): Represents an OR clause in conditions
- Condition (Class): Represents an individual condition
- SidesList (Class): Not inferable

## Key Functions
### ScriptConditionsDlg::DoDataExchange
- Purpose: Handles data exchange between dialog controls and member variables
- Calls: CDataExchange methods

### ScriptConditionsDlg::setScript
- Purpose: Sets the script being edited
- Calls: None

### ScriptConditionsDlg::enableUI
- Purpose: Enables/disables UI controls based on current selection
- Calls: Not inferable

### ScriptConditionsDlg::loadList
- Purpose: Populates the condition list UI control
- Calls: Not inferable

### ScriptConditionsDlg::doMoveUp
- Purpose: Moves a condition up in the list
- Calls: Not inferable

### ScriptConditionsDlg::doMoveDown
- Purpose: Moves a condition down in the list
- Calls: Not inferable

### ScriptConditionsDlg::setSel
- Purpose: Sets the current selection in the dialog
- Calls: Not inferable

### ScriptConditionsDlg::OnInitDialog
- Purpose: Initializes the dialog
- Calls: enableUI, loadList

### ScriptConditionsDlg::OnEditCondition
- Purpose: Handles editing of the selected condition
- Calls: Not inferable
