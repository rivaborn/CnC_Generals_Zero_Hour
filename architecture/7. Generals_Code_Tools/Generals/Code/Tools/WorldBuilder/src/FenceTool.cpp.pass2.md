# Generals/Code/Tools/WorldBuilder/src/FenceTool.cpp - Enhanced Analysis

## Architectural Role
This file implements the fence placement tool in WorldBuilder, a key component of the level editing pipeline. It bridges the UI interaction layer with the map object system, enabling non-programmers to place fenced structures efficiently.

## Cross-References
### Incoming
- `CMainFrame::GetMainFrame()` - Called during activation to show options dialog
- `ObjectOptions::duplicateCurMapObjectForPlace()` - Used for creating fence segments
- `FenceOptions::update()` - Called during activation and mouse events
- `WbView3d::setObjTracking()` - Used for visual feedback during placement
- `CWorldBuilderDoc::AddAndDoUndoable()` - Used for committing changes

### Outgoing
- `WbView::viewToDocCoords()` - Converts screen to world coordinates
- `WbView::snapPoint()` - Applies grid snapping to placement
- `WbView3d::removeFenceListObjects()` - Cleans up temporary objects
- `WbView3d::updateFenceListObjects()` - Updates visual representation

## Design Patterns
- **Command Pattern**: Encapsulates fence placement as an undoable operation via `AddObjectUndoable`
- **Observer Pattern**: Listens to mouse events and updates visual feedback in real-time
- **Flyweight Pattern**: Reuses `MapObject` instances for fence segments to reduce memory usage

*Not inferable*: Exact implementation of `Coord3D` operations (normalization, length calculation)
