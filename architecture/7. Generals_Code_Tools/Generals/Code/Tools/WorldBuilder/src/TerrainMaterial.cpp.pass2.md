# Generals/Code/Tools/WorldBuilder/src/TerrainMaterial.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI and logic for terrain material editing in WorldBuilder, bridging the gap between the editor's UI layer and the underlying terrain rendering system. It manages texture selection, brush tools, and passability settings, acting as a controller for terrain modification operations.

## Cross-References
### Incoming
- **TileTool.h**: Uses `BigTileTool::setWidth()` to propagate brush size changes
- **WBView3D.h**: Calls `updateHeightMapInView()` to refresh terrain rendering
- **WorldBuilderDoc.h**: Accesses `GetActiveDoc()` and `GetHeightMap()` for document state

### Outgoing
- **W3DDevice/GameClient/TerrainTex.h**: Relies on terrain texture management
- **W3DDevice/GameClient/HeightMap.h**: Uses heightmap editing interfaces
- **Common/TerrainTypes.h**: Depends on terrain type definitions

## Design Patterns
- **Singleton**: Uses `m_staticThis` for global access to the dialog instance
- **Observer**: Handles UI events via `OnNotify()` for tree view changes
- **Mediator**: Coordinates between UI controls (tree view, swatches, sliders) and terrain data

*Not inferable: No clear use of Factory, Strategy, or Command patterns in visible code.*
