# Generals/Code/Tools/WorldBuilder/include/ScriptProperties.h

## Purpose
Header file for the ScriptProperties dialog class used in WorldBuilder to edit script properties.

## Responsibilities
- Manages UI for script properties (name, comment, triggers, timing)
- Handles data exchange between UI controls and script object
- Enables/disables controls based on script type
- Processes user input events for script properties

## Key Types
- Script (Class): Reference to the script being edited
- ScriptProperties (Class): Dialog for editing script properties
- (anonymous enum) (Enum): Contains IDD_ScriptProperties dialog ID
- IDD (Enum): Dialog resource identifier

## Key Functions
### ScriptProperties::OnSetActive
- Purpose: Called when the dialog becomes active
- Calls: enableControls

### ScriptProperties::DoDataExchange
- Purpose: Handles data exchange between UI controls and script object
- Calls: Not inferable

### ScriptProperties::setScript
- Purpose: Sets the script object being edited
- Calls: None

### ScriptProperties::enableControls
- Purpose: Enables/disables controls based on script type
- Calls: None

### ScriptProperties::OnChangeScriptComment
- Purpose: Handles changes to script comment field
- Calls: None

### ScriptProperties::OnChangeScriptName
- Purpose: Handles changes to script name field
- Calls: None

### ScriptProperties::OnScriptActive
- Purpose: Handles changes to script active checkbox
- Calls: None

### ScriptProperties::OnOneShot
- Purpose: Handles changes to one-shot script type radio button
- Calls: None

### ScriptProperties::OnEasy
- Purpose: Handles changes to easy script type radio button
- Calls: None

### ScriptProperties::OnHard
- Purpose: Handles changes to hard script type radio button
- Calls:
