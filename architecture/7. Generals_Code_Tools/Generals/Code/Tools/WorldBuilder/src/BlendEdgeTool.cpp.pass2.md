# Generals/Code/Tools/WorldBuilder/src/BlendEdgeTool.cpp - Enhanced Analysis

## Architectural Role
This file implements a specialized tool in the WorldBuilder editor's toolchain, bridging user input with terrain texture manipulation. It extends the base `Tool` class to handle texture blending operations, integrating with the document-view architecture for coordinate translation and undo/redo management.

## Cross-References
### Incoming
- **Tool Framework**: Likely instantiated by the WorldBuilder tool manager (e.g., `CMainFrame` or tool palette) when the blend edge tool is selected.
- **Undo System**: `WBDocUndoable` is created here but managed by `CWorldBuilderDoc`, indicating a dependency on the document's undo/redo infrastructure.

### Outgoing
- **View System**: Calls `WbView::viewToDocCoords` for coordinate conversion, showing tight coupling with the view layer.
- **Document System**: Relies on `CWorldBuilderDoc` for cell index lookup and height map updates.
- **Height Map Editing**: Uses `WorldHeightMapEdit` for actual blending operations, demonstrating a clear separation between tool logic and terrain data manipulation.

## Design Patterns
- **Command Pattern**: The tool encapsulates a user action (blend operation) as an object (`WBDocUndoable`), enabling undo/redo functionality.
- **Mediator Pattern**: The tool mediates between user input (mouse events) and the underlying terrain data (`WorldHeightMapEdit`), abstracting the complexity of texture blending.
- **Prototype Pattern**: Uses `duplicate()` to create a copy of the height map before applying changes, ensuring the original remains unmodified until the operation is confirmed.
