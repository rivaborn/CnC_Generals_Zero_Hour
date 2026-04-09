# Generals/Code/Tools/WorldBuilder/src/WorldBuilderView.cpp - Enhanced Analysis

## Architectural Role
This file implements the core 2D view rendering system for WorldBuilder, bridging the MFC-based UI framework with the game's terrain editing pipeline. It handles coordinate transformations between screen and world space, which is critical for both the editor's usability and the underlying heightmap data integrity.

## Cross-References
### Incoming
- **WorldBuilderDoc.cpp**: Calls `viewToDocCoords`/`docToViewCoords` for coordinate conversions during editing operations
- **MainFrm.cpp**: Uses `OnShowGrid`/`OnViewShowtexture` handlers for menu state synchronization
- **WHeightMapEdit.cpp**: Relies on `getColorForHeight` for terrain visualization

### Outgoing
- **W3DDevice/GameClient/HeightMap.h**: Uses `WorldHeightMapEdit` for terrain data access
- **Common/Debug.h**: For coordinate transformation validation assertions
- **MFC framework**: For view rendering, scrolling, and message handling

## Design Patterns
- **View-Model separation**: The view class (`CWorldBuilderView`) delegates terrain data access to `WorldHeightMapEdit` while handling only presentation logic
- **Coordinate transformation adapter**: `viewToDocCoords`/`docToViewCoords` act as adapters between pixel and world coordinates, abstracting the conversion logic
- **Observer pattern**: Menu state updates via `OnUpdateShowGrid`/`OnUpdateViewShowtexture` reflect the view's current state (not inferable if these are direct calls or event-driven)
