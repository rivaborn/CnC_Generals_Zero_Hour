# Generals/Code/Tools/WorldBuilder/include/BlendMaterial.h - Enhanced Analysis

## Architectural Role
This header defines the UI component for terrain texture blending in WorldBuilder, bridging the terrain editing tools with the rendering pipeline. It encapsulates the dialog logic for selecting and managing blend textures, which are critical for terrain visualization in the SAGE engine.

## Cross-References
### Incoming
- Likely called by `WorldHeightMapEdit` (forward-declared dependency) for terrain editing operations.
- May be referenced by other WorldBuilder tools that require terrain texture manipulation.

### Outgoing
- Depends on `WBPopupSlider.h` for slider controls in the UI.
- Uses `TerrainSwatches.h` for terrain texture management.
- Inherits from `COptionsPanel`, indicating integration with the WorldBuilder options system.

## Design Patterns
- **Singleton-like Access**: Uses a static instance pointer (`m_staticThis`) for global access, common in MFC dialogs.
- **Observer Pattern**: The `OnNotify` override suggests event-driven updates, typical for UI components.
- **Composite Pattern**: The tree view structure (`CTreeCtrl`) implies hierarchical terrain organization, aligning with terrain layering in the SAGE engine.
