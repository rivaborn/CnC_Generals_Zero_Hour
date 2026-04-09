# Generals/Code/Tools/WorldBuilder/include/WorldBuilderDoc.h

## Purpose
Defines the `CWorldBuilderDoc` class, the core document class for the WorldBuilder tool, managing map data, undo/redo operations, and view synchronization.

## Responsibilities
- Manages map document state (heightmap, waypoints, boundaries)
- Handles undo/redo functionality
- Synchronizes 2D/3D views
- Provides map serialization/deserialization
- Manages waypoint and boundary data

## Key Types
- `CWorldBuilderDoc` (Class): Main document class for WorldBuilder
- `Undoable` (Class): Base class for undoable operations
- `DataChunkInput` (Class): Data chunk input interface
- `DataChunkInfo` (Struct): Data chunk metadata
- `(anonymous enum)` (Enum): Contains `MAX_WAYPOINTS` constant
- `(anonymous struct)` (Struct): Waypoint link data structure

## Key Functions
### `addWaypointLink`
- Purpose: Adds a link between two waypoints
- Calls: None visible

### `removeWaypointLink`
- Purpose: Removes a link between two waypoints
- Calls: None visible

### `updateWaypointTable`
- Purpose: Updates the waypoint table
- Calls: None visible

### `autoSave`
- Purpose: Performs an automatic save of the document
- Calls: None visible

### `AddAndDoUndoable`
- Purpose: Adds an undoable operation to the undo stack and executes it
- Calls: None visible

## Globals
- `MAX_UNDOS` (const int): Maximum number of undo operations stored
- `MIN_CELL_SIZE` (const int): Minimum cell size for the map
- `MAX_CELL_SIZE` (const int): Maximum cell size for the map

## Dependencies
- `lib/BaseType.h`
- `Common/MapObject.h`
- `Tool.h`
- `CDocument` (MFC class)
- `CWorldBuilderView`, `WbView3d`, `WorldHeightMapEdit`, `Undoable`, `DataChunkInput`, `DataChunkInfo` (forward declarations)
