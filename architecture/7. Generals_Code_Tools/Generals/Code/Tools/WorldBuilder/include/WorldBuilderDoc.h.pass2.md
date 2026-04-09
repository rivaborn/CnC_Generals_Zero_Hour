# Generals/Code/Tools/WorldBuilder/include/WorldBuilderDoc.h - Enhanced Analysis

## Architectural Role
This file defines the core document class for WorldBuilder, acting as the central data manager for map editing. It bridges the MFC document-view architecture with SAGE engine-specific map data structures, handling serialization, undo/redo, and view synchronization.

## Cross-References
### Incoming
- `CWorldBuilderView` (2D view) and `WbView3d` (3D view) classes use this for document access
- `Undoable` operations are registered here for undo/redo functionality
- `DataChunkInput` parsing calls `ParseWaypointDataChunk` for waypoint serialization

### Outgoing
- Calls into `WorldHeightMapEdit` for terrain manipulation
- Uses `MapObject` for waypoint/boundary storage
- Interfaces with MFC's `CDocument` for standard document operations

## Design Patterns
- **Command Pattern**: `Undoable` operations encapsulate actions for undo/redo
- **Mediator Pattern**: Centralizes view synchronization and document state
- **Singleton-like Access**: Static `GetActiveDoc()` provides global document access (not pure singleton)
