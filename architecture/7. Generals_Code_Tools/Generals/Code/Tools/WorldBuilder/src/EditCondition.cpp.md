# Generals/Code/Tools/WorldBuilder/src/EditCondition.cpp

## Purpose
Handles the UI for editing script conditions in WorldBuilder, a level editing tool.

## Responsibilities
- Manages a dialog for editing script conditions
- Displays and formats condition text with parameter links
- Handles parameter editing via rich edit control
- Updates UI based on condition type selection

## Key Types
- **EditCondition (class)**: Dialog class for editing script conditions
- **ConditionTemplate (struct)**: Not inferable (external)
- **Condition (class)**: Represents a script condition (external)

## Key Functions
### `OnInitDialog`
- Purpose: Initializes the dialog, sets up controls and populates condition type combo box
- Calls: `TheScriptEngine->getConditionTemplate`, `m_condition->getConditionType`, `m_condition->setWarnings`, `m_condition->getUiText`, `formatConditionText`

### `formatConditionText`
- Purpose: Formats the condition text with colored parameter links and warning messages
- Calls: `m_condition->getUiStrings`, `m_condition->getNumParameters`, `m_condition->getParameter`, `EditParameter::getWarningText`, `m_condition->getUiText`

### `OnNotify`
- Purpose: Handles rich edit control notifications (links and selection changes)
- Calls: `EditParameter::edit`, `formatConditionText`

### `OnSelchangeConditionType`
- Purpose: Updates condition type when combo box selection changes
- Calls: `TheScriptEngine->getConditionTemplate`, `m_condition->setConditionType`, `m_condition->getUiText`, `formatConditionText`

### `OnTimer`
- Purpose: Handles delayed formatting after parameter editing
- Calls: `formatConditionText`

## Globals
- **TheScriptEngine (ScriptEngine**)**: Global script engine instance

## Dependencies
- `stdafx.h`, `worldbuilder.h`, `EditCondition.h`, `EditParameter.h`, `GameLogic/ScriptEngine.h`
- MFC classes: `CDialog`, `CWnd`, `CComboBox`, `CRichEditCtrl`
- External types: `Condition`, `ConditionTemplate`, `ScriptAction`
