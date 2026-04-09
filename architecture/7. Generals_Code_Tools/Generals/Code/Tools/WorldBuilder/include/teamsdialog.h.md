# Generals/Code/Tools/WorldBuilder/include/teamsdialog.h

## Purpose
Header for the CTeamsDialog class, which manages team configuration in the WorldBuilder tool.

## Responsibilities
- Manages team creation, deletion, and editing
- Handles team member selection and team ordering
- Validates team ownership and alliances
- Updates UI elements based on team changes

## Key Types
- **CTeamsDialog (Class)**: Dialog for managing teams in WorldBuilder
- **IDD (Enum)**: Dialog resource ID
- **REBUILD_TEAMS (Enum)**: Flag for rebuilding teams list
- **REBUILD_OWNERS (Enum)**: Flag for rebuilding owners list
- **REBUILD_ALLIES (Enum)**: Flag for rebuilding allies list
- **REBUILD_NONE (Enum)**: Flag for no rebuild
- **REBUILD_ALL (Enum)**: Flag for rebuilding all

## Key Functions
### CTeamsDialog()
- Purpose: Constructor for CTeamsDialog
- Calls: None

### DoDataExchange()
- Purpose: Handles data exchange for the dialog
- Calls: None

### OnInitDialog()
- Purpose: Initializes the dialog
- Calls: None

### OnOK()
- Purpose: Handles OK button click
- Calls: None

### OnCancel()
- Purpose: Handles Cancel button click
- Calls: None

### OnNewteam()
- Purpose: Creates a new team
- Calls: None

### OnDeleteteam()
- Purpose: Deletes the selected team
- Calls: None

### OnEditTemplate()
- Purpose: Edits the team template
- Calls: None

### OnSelchangePlayerList()
- Purpose: Handles player list selection change
- Calls: None

### OnClickTeamsList()
- Purpose: Handles team list click
- Calls: None

### OnDblclkTeamsList
