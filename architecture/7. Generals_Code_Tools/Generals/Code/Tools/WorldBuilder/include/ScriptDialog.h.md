# Generals/Code/Tools/WorldBuilder/include/ScriptDialog.h

## Purpose
Header for the ScriptDialog class, which manages script editing in the WorldBuilder tool.

## Responsibilities
- Defines UI dialog for script editing
- Manages script tree view with drag-and-drop
- Handles script parsing and validation
- Provides access to script objects and groups

## Key Types
- **ListType (Class)**: Encodes script object types (player/group/script) into packed integer
- **CSDTreeCtrl (Class)**: Custom tree control with right-click context menu support
- **ScriptDialog (Class)**: Main dialog class for script editing interface
- **BOGUS_TYPE/PLAYER_TYPE/GROUP_TYPE/SCRIPT_IN_PLAYER_TYPE/SCRIPT_IN_GROUP_TYPE (Enum)**: Script object type identifiers

## Key Functions
### `ListToInt()`
- Purpose: Packs ListType fields into a single integer
- Calls: None

### `IntToList()`
- Purpose: Unpacks integer into ListType fields
- Calls: None

### `updateWarnings()`
- Purpose: Updates script warnings in the UI
- Calls: `updateScriptWarning()`

### `ParseObjectsDataChunk()`
- Purpose: Parses object data chunks from files
- Calls: None (static callback)

## Globals
- **m_staticThis (ScriptDialog*)**: Static pointer to the dialog instance
- **m_curSelection (ListType)**: Tracks current tree selection

## Dependencies
- `GameLogic/SidesList.h`
- MFC classes (CDialog, CTreeCtrl, etc.)
- DataChunkInput/DataChunkInfo for file parsing
