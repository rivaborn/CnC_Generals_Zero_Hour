# Generals/Code/Tools/WorldBuilder/src/teamsdialog.cpp

## Purpose
Manages the teams dialog in WorldBuilder, allowing users to create, edit, and manage game teams.

## Responsibilities
- Display and edit team properties via UI
- Handle team creation, deletion, and reordering
- Validate team ownership relationships
- Synchronize UI with underlying team data

## Key Types
- **CTeamsDialog (class)**: Main dialog class for team management
- **SidesList (struct)**: Contains team and side information
- **TeamsInfo (struct)**: Represents a team's properties

## Key Functions
### isPlayerDefaultTeamIndex
- Purpose: Checks if a team is a default player team
- Calls: sides.isPlayerDefaultTeam

### teamNameForUI
- Purpose: Formats a team name for display
- Calls: ti->getDict()->getAsciiString

### UIToInternal
- Purpose: Converts UI display name to internal name
- Calls: playerNameForUI, sides.getSideInfo

### findTeamParentIndex
- Purpose: Finds the parent team index for a given team
- Calls: sides.getTeamInfo, sides.getSideInfo

### updateUI
- Purpose: Refreshes the dialog UI based on current state
- Calls: UpdateTeamsList, m_sides.validateSides

### OnEditTemplate
- Purpose: Opens property sheets for editing team details
- Calls: TeamIdentity, TeamReinforcement, TeamBehavior constructors

### OnSelectTeamMembers
- Purpose: Selects all map objects belonging to a team
- Calls: MapObject::getFirstMapObject, pObj->setSelected

## Globals
- **thePrevCurTeam (Int)**: Stores the previously selected team index
- **NEUTRAL_NAME_STR (const char*)**: String for neutral team display

## Dependencies
- MFC dialog framework (CDialog, CListCtrl)
- Game logic: SidesList, TeamsInfo, Dict
- UI: Common/WellKnownKeys.h
- Undo system: SidesListUndoable, CUndoable
- 3D view: WBView3d
