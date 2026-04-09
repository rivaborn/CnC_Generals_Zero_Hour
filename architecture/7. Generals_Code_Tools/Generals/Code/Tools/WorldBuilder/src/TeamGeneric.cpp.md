# Generals/Code/Tools/WorldBuilder/src/TeamGeneric.cpp

## Purpose
Handles the UI and data management for team-specific script hooks in the WorldBuilder tool.

## Responsibilities
- Manages 16 script hook combo boxes in the UI
- Synchronizes UI state with a dictionary of team settings
- Loads available scripts into combo boxes
- Handles user selection changes and updates the dictionary

## Key Types
- `TeamGeneric` (Class): Property page for team script hooks
- `s_allControls` (Array): Maps UI control IDs to script hook IDs

## Key Functions
### `OnInitDialog`
- Purpose: Initializes the dialog and populates script combo boxes
- Calls: `_fillComboBoxesWithScripts`, `_dictToScripts`

### `_fillComboBoxesWithScripts`
- Purpose: Loads available scripts into all combo boxes
- Calls: `EditParameter::loadScripts`

### `_dictToScripts`
- Purpose: Updates UI controls from the team dictionary
- Calls: `m_teamDict->getAsciiString`

### `_scriptsToDict`
- Purpose: Updates the team dictionary from UI controls
- Calls: `m_teamDict->setAsciiString`, `m_teamDict->remove`

### `OnScriptAdjust`
- Purpose: Handles script selection changes
- Calls: `_scriptsToDict`, `_dictToScripts`

## Globals
- `s_allControls` (Array): Maps UI control IDs to script hook IDs

## Dependencies
- `TeamGeneric.h`, `EditParameter.h`, `WorldBuilder.h`
- `Common/AsciiString.h`, `Common/Dict.h`, `Common/WellKnownKeys.h`
- MFC classes (`CPropertyPage`, `CComboBox`, etc.)
- `TheNameKeyGenerator`, `TheKey_teamGenericScriptHook`
