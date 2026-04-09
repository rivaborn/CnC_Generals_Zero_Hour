# Generals/Code/Tools/WorldBuilder/src/FloodFillTool.cpp - Enhanced Analysis

## Architectural Role
This file implements a terrain editing tool in WorldBuilder, bridging the UI layer with the terrain modification subsystem. It handles user input for flood-fill operations and cliff adjustments, while integrating with the undo/redo system and terrain material selection.

## Cross-References
### Incoming
- **UI Layer**: `CMainFrame` calls `activate()` to show tool options
- **View Layer**: `WbView` calls `mouseUp()` for coordinate conversion
- **Document Layer**: `CWorldBuilderDoc` calls `mouseUp()` for terrain updates

### Outgoing
- **UI Layer**: Calls `CMainFrame::showOptionsDialog()` and `AfxGetApp()->LoadCursor()`
- **Terrain Layer**: Calls `WorldHeightMapEdit::floodFill()` and `doCliffAdjustment()`
- **Undo System**: Calls `WBDocUndoable` constructor and `pDoc->AddAndDoUndoable()`

## Design Patterns
- **Command Pattern**: Encapsulates flood-fill operation in `WBDocUndoable` for undo/redo
- **State Pattern**: Cursor behavior changes based on `m_adjustCliffTextures` flag
- **Mediator Pattern**: Coordinates between UI, view, and document layers without direct coupling
