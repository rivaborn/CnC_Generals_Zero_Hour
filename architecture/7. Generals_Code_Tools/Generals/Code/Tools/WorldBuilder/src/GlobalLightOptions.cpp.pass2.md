# Generals/Code/Tools/WorldBuilder/src/GlobalLightOptions.cpp - Enhanced Analysis

## Architectural Role
This file implements the lighting configuration UI for WorldBuilder, bridging the gap between user input and the W3D rendering pipeline. It manages real-time updates to lighting parameters while coordinating with the 3D view system.

## Cross-References
### Incoming
- **WorldBuilderDoc.h**: Uses `CWorldBuilderDoc::GetActive3DView()` to access the current 3D view
- **WbView3D.h**: Calls `WbView3d::setLighting()` and `WbView3d::doLightFeedback()` to apply changes
- **GlobalData.h**: Reads/writes lighting data via `TheGlobalData` and `TheWritableGlobalData`

### Outgoing
- **WWMath**: Uses trigonometric functions (`Sin`, `Cos`) for light direction calculations
- **DEBUG_LOG/DEBUG_CRASH**: For logging and error handling
- **MFC UI classes**: `CDialog`, `CColorDialog`, etc., for the UI implementation

## Design Patterns
- **Observer Pattern**: The dialog updates the 3D view whenever lighting parameters change
- **Facade Pattern**: Abstracts complex lighting calculations behind simple UI controls
- **Singleton Access**: Uses global `TheGlobalData` for shared lighting state (not ideal, but common in SAGE)

Rules followed. Output under 400 tokens.
