# Generals/Code/Tools/WorldBuilder/src/ScriptDialog.cpp

## Purpose
Handles the ScriptDialog UI in WorldBuilder, managing game scripts, groups, and player teams.

## Responsibilities
- Manages script/group tree view with drag-and-drop
- Handles script activation/toggling
- Imports/exports script data (waypoints, teams, triggers)
- Updates warning flags for scripts/conditions/actions
- Maintains player/team hierarchy in the UI

## Key Types
- **LocalMFCFileOutputStream (Class)**: Wraps MFC file output for script export
- **ScriptDialog (Class)**: Main dialog class for script management
- **CSDTreeCtrl (Class)**: Custom tree control for script/group display

## Key Functions
### formatScriptLabel (Script*)
- Purpose: Formats script label with status flags (active/oneshot/difficulty)
- Calls: None

### formatScriptLabel (ScriptGroup*)
- Purpose: Formats group label with status flags
- Calls: None

### updateScriptWarning (Script*)
- Purpose: Updates warning flags for script conditions/actions
- Calls: EditParameter::getWarningText

### ParseTeamsDataChunk
- Purpose: Parses team data from chunked file format
- Calls: m_sides.findTeamInfo, m_sides.addTeam

### OnScriptActivate
- Purpose: Toggles script/group active state and updates UI
- Calls: getCurScript, getCurGroup, pTree->SetItemText

## Globals
- **K_LOCAL_TEAMS_VERSION_1 (Int)**: Version constant for team data
- **NEUTRAL_NAME_STR (char**)**: String for neutral player name
- **m_staticThis (ScriptDialog**)**: Static pointer to dialog instance

## Dependencies
- MFC UI classes (CDialog, CTreeCtrl)
- Game logic: ScriptEngine, SidesList, PolygonTrigger
- Common: DataChunk, FileSystem, UnicodeString
- WorldBuilder-specific: CUndoable, EditParameter, ExportScriptsOptions
