# Generals/Code/Tools/WorldBuilder/src/WaterTool.cpp - Enhanced Analysis

## Architectural Role
This file implements the water editing tool in WorldBuilder, bridging the gap between the editor's UI and the game's terrain system. It handles water polygon creation/modification while integrating with the undo system and terrain heightmap.

## Cross-References
### Incoming
- **WorldBuilderDoc**: Calls `fillTheArea` and `adjustSpacing` during water area creation
- **WorldBuilderView**: Uses `mapZtoHeight` for coordinate conversion
- **PointerTool**: Inherits behavior for polygon selection/dragging

### Outgoing
- **GameLogic/PolygonTrigger**: Creates/modifies water polygons
- **CUndoable**: Generates undo actions for water edits
- **WHeightMapEdit**: Accesses terrain height data via `mapZtoHeight`

## Design Patterns
- **Command Pattern**: Encapsulates water operations in `AddPolygonUndoable` for undo/redo
- **State Pattern**: Tracks tool state via flags (`m_water_isActive`, `m_poly_isAdding`)
- **Strategy Pattern**: `adjustSpacing` implements polygon point distribution as a configurable strategy

*Not inferable*: Exact relationship with `DrawObject::setDoBrushFeedback` (likely UI feedback suppression).
