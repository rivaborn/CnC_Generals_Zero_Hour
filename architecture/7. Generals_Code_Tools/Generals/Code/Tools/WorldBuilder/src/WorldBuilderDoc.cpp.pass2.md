# Generals/Code/Tools/WorldBuilder/src/WorldBuilderDoc.cpp - Enhanced Analysis

## Architectural Role
Core document class for WorldBuilder, bridging MFC document architecture with SAGE engine map data structures. Acts as the central mediator between UI commands and underlying map data, implementing the document-view pattern with undo/redo support.

## Cross-References
### Incoming
- UI command handlers (e.g., `OnEditUndo`, `OnFileResize`)
- View classes (`WorldBuilderView`, `WbView3d`) for map rendering
- Main frame (`MainFrm`) for menu updates

### Outgoing
- `WorldHeightMap` for terrain operations
- `ScriptEngine` for map scripting
- `ThingFactory` for object placement
- `Compression` for map file handling

## Design Patterns
- **Document-View**: Manages map data independently of views
- **Command Pattern**: Encapsulates operations in `CUndoable` for undo/redo
- **Recursive Template Method**: In `AddUniqueAndNeighbors` for region selection

*Not inferable*: Specific compression algorithm or MFC integration details.
