# Generals/Code/Tools/WorldBuilder/src/GroveTool.cpp - Enhanced Analysis

## Architectural Role
This file implements the grove placement tool in WorldBuilder, bridging the gap between terrain editing and object placement. It validates terrain suitability (cliffs, water, slope) before placing trees/shrubs, using the heightmap and polygon triggers for spatial queries.

## Cross-References
### Incoming
- `WorldBuilderDoc.h` (uses `AddObjectUndoable` for undo/redo)
- `WorldBuilderView.h` (handles view coordinate conversion)
- `GroveOptions.h` (reads tree placement configuration)

### Outgoing
- `GameLogic/LogicRandomValue.h` (for random tree selection)
- `W3DDevice/GameClient/HeightMap.h` (terrain height queries)
- `GameLogic/PolygonTrigger.h` (water area detection)

## Design Patterns
- **Strategy Pattern**: Tree placement logic varies based on terrain conditions (cliffy, underwater), encapsulated in validation functions.
- **Composite Pattern**: `plantGrove` recursively builds groves from seed locations, treating each tree as part of a larger structure.
- **Observer Pattern**: Tool activation shows options dialog via `CMainFrame::GetMainFrame()->showOptionsDialog`, decoupling UI from tool logic.
