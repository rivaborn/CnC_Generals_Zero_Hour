# Generals/Code/Tools/WorldBuilder/include/CFixTeamOwnerDialog.h

## Purpose
Defines a dialog class for selecting and assigning team ownership in the WorldBuilder tool.

## Responsibilities
- Manages team owner selection UI
- Validates team owner picks
- Stores selected owner and validation state
- Interfaces with TeamsInfo and SidesList data structures

## Key Types
- CFixTeamOwnerDialog (Class): Dialog for team owner assignment
- TeamsInfo (Class): External team information container
- SidesList (Class): External side/listing container
- (anonymous enum) (Enum): Contains IDD constant for dialog template ID

## Key Functions
### CFixTeamOwnerDialog()
- Purpose: Constructor initializing dialog with team info and side list.
- Calls: None

### getSelectedOwner()
- Purpose: Returns the selected owner as an AsciiString.
- Calls: None

### pickedValidTeam()
- Purpose: Returns whether a valid team was picked.
- Calls: None

### OnInitDialog()
- Purpose: Initializes dialog controls and data.
- Calls: Not inferable

### OnOK()
- Purpose: Handles OK button click, validates selection.
- Calls: Not inferable

## Globals
- None

## Dependencies
- Common/AsciiString.h
- CDialog (MFC class)
- TeamsInfo (forward declared)
- SidesList (forward
