# Generals/Code/Tools/WorldBuilder/src/EditAction.cpp

## Purpose
Handles the UI for editing script actions in WorldBuilder, a level editor tool.

## Responsibilities
- Manages a dialog for editing script actions
- Formats and displays action parameters with clickable links
- Handles parameter editing via rich edit control
- Updates UI based on action type selection

## Key Types
- **EditAction (class)**: Main dialog class for editing script actions
- **ScriptAction (enum)**: Not defined here, but used for action types
- **ActionTemplate (struct)**: Not defined here, provides action templates

## Key Functions
### EditAction::OnInitDialog
- Purpose: Initializes the dialog and sets up controls
- Calls: `TheScriptEngine->getActionTemplate`, `m_action->setWarnings`, `formatScriptActionText`

### EditAction::formatScriptActionText
- Purpose: Formats the script action text with colored parameters
- Calls: `m_action->getUiStrings`, `EditParameter::getWarningText`, `EditParameter::getInfoText`

### EditAction::OnNotify
- Purpose: Handles rich edit control notifications (links and selection changes)
- Calls: `EditParameter::edit`, `formatScriptActionText`

### EditAction::OnSelchangeScriptActionType
- Purpose: Updates the action type when the combo box selection changes
- Calls: `TheScriptEngine->getActionTemplate`, `formatScriptActionText`

### EditAction::OnTimer
- Purpose: Handles delayed formatting after parameter editing
- Calls: `formatScriptActionText`

## Globals
- **TheScriptEngine (ScriptEngine**)**: Global script engine instance

## Dependencies
- `EditAction.h`, `EditParameter.h`, `GameLogic/ScriptEngine.h`
- MFC classes (`CDialog`, `CComboBox`, `CRichEditCtrl`)
- `AsciiString` class for string handling
