# Generals/Code/Tools/WorldBuilder/include/EditCondition.h

## Purpose
Header for the `EditCondition` dialog class used in WorldBuilder to edit script conditions.

## Responsibilities
- Manages UI for editing conditions in game scripts
- Handles condition type selection and parameter editing
- Formats condition text for display
- Updates condition data based on user input

## Key Types
- **Condition (Class)**: Base class for script conditions.
- **SidesList (Class)**: Not inferable.
- **EditCondition (Class)**: Dialog for editing script conditions.
- **(anonymous enum) (Enum)**: Dialog resource ID.
- **IDD (Enum)**: Dialog resource ID.

## Key Functions
### `EditCondition::DoDataExchange`
- Purpose: Handles data exchange between dialog controls and member variables.
- Calls: Not inferable.

### `EditCondition::OnNotify`
- Purpose: Processes notification messages from dialog controls.
- Calls: Not inferable.

### `EditCondition::setCondition`
- Purpose: Sets the condition object to edit.
- Calls: None.

### `EditCondition::formatConditionText`
- Purpose: Formats the condition text for display in the rich edit control.
- Calls: None.

### `EditCondition::OnInitDialog`
- Purpose: Initializes the dialog when it is created.
- Calls: Not inferable.

### `EditCondition::OnSelchangeConditionType`
- Purpose: Handles changes in the condition type selection.
- Calls: Not inferable.

### `EditCondition::OnTimer`
- Purpose: Handles timer events for the dialog.
- Calls: Not inferable.

## Globals
- **m_condition (Condition*)**: Pointer to the condition being edited.
- **m_updating (Bool)**: Flag indicating if the dialog is updating.
- **m_modifiedTextColor (Bool)**: Flag for text color modification.
- **m_myEditCtrl (CRich
