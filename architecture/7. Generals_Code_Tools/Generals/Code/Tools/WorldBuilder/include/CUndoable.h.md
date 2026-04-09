# Generals/Code/Tools/WorldBuilder/include/CUndoable.h

## Purpose
Defines the undo/redo command framework for the WorldBuilder tool, including base and derived undoable command classes.

## Responsibilities
- Provides base `Undoable` class for undo/redo operations
- Implements specialized undoable commands for map editing (objects, polygons, flags, etc.)
- Manages state tracking for modifications (positions, templates, flags, etc.)
- Supports chaining of undoable commands
- Handles document-level undo/redo operations

## Key Types
- **Undoable (Class)**: Base abstract class for undoable commands
- **WBDocUndoable (Class)**: Handles entire heightmap undo/redo
- **AddObjectUndoable (Class)**: Manages object addition/removal
- **ModifyObjectUndoable (Class)**: Tracks object property changes
- **MoveInfo (Class)**: Helper for object movement state
- **ModifyFlagsUndoable (Class)**: Handles object flag modifications
- **FlagsInfo (Class)**: Helper for flag state tracking
- **DeleteObjectUndoable (Class)**: Manages object deletion
- **AddPolygonUndoable (Class)**: Handles polygon addition
- **ModifyPolygonPointUndoable (Class)**: Tracks polygon point modifications
- **MovePolygonUndoable (Class)**: Manages polygon movement
- **DeletePolygonUndoable (Class)**: Handles polygon deletion

## Key Functions
### Undoable::Redo
- Purpose: Default redo implementation that calls Do()
- Calls: Do()

### WBDocUndoable::Do/Undo/Redo
- Purpose: Applies/restores heightmap changes
- Calls: CWorldBuilderDoc methods

### ModifyObjectUndoable::SetOffset/RotateTo/SetThingTemplate/SetName
- Purpose: Configures object modification parameters
- Calls: MoveInfo methods

### MoveInfo::DoMove/UndoMove
- Purpose: Applies/reverts object movement
- Calls: CWorldBuilderDoc methods

## Globals
None

## Dependencies
- `RefCount.h` (memory management)
- `MapObject.h` (game object definitions)
- `GameCommon.h` (common game types)
- `SidesList.h` (team/side management)
- `PolygonTrigger` (forward declaration)
- `BuildListInfo` (forward declaration)
