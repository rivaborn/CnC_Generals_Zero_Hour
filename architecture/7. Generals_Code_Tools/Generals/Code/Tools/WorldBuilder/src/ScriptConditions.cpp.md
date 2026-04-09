# Generals/Code/Tools/WorldBuilder/src/ScriptConditions.cpp

## Purpose
Handles the UI and logic for editing script conditions in the WorldBuilder tool.

## Responsibilities
- Manages the ScriptConditions property page dialog
- Handles condition list display and selection
- Implements condition editing, creation, deletion, and reordering
- Updates the script warning display when conditions change

## Key Types
- **ScriptConditionsDlg (Class)**: Main dialog class for condition editing
- **Condition (Class)**: Represents a single condition in a script
- **OrCondition (Class)**: Represents an OR group of conditions
- **Script (Class)**: The script being edited (referenced via m_script)

## Key Functions
### OnEditCondition
- Purpose: Opens the EditCondition dialog for the selected condition
- Calls: EditCondition::DoModal, ScriptDialog::updateScriptWarning

### OnNew
- Purpose: Creates a new condition and adds it to the current OR group
- Calls: newInstance, EditCondition::DoModal, Condition::deleteInstance

### OnDelete
- Purpose: Removes the selected condition or OR group
- Calls: OrCondition::deleteCondition, Script::deleteOrCondition

### doMoveDown/doMoveUp
- Purpose: Moves conditions/OR groups up or down in the list
- Calls: OrCondition::removeCondition, Condition::setNextCondition, etc.

### OnChangeEditComment
- Purpose: Updates the script's condition comment text
- Calls: Script::setConditionComment

## Globals
- **m_script (Script*)**: Pointer to the script being edited
- **m_condition (Condition*)**: Currently selected condition
- **m_orCondition (OrCondition*)**: Currently selected OR group
- **m_index (Int)**: Index of the selected item in the list

## Dependencies
- "worldbuilder.h", "ScriptConditions.h", "GameLogic/Scripts.h", "EditCondition.h", "ScriptDialog.h"
- Uses MFC classes (CPropertyPage, CListBox, etc.)
- Depends on Script, Condition, OrCondition classes from game logic
