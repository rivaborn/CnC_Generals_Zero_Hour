# Generals/Code/Tools/WorldBuilder/include/TerrainMaterial.h - Enhanced Analysis

## Architectural Role
This header defines the `TerrainMaterial` class, a key component of WorldBuilder's terrain editing UI. It bridges the gap between user input (via dialog controls) and the underlying terrain data model, facilitating texture selection, brush size adjustment, and pathing/passability editing.

## Cross-References
### Incoming
- **WorldBuilder UI modules**: Likely called by main WorldBuilder window or terrain editing tools to display/modify terrain properties.
- **TerrainSwatches**: Uses `TerrainSwatches` for visual texture previews (included header).
- **WBPopupSlider**: Inherits from `PopupSliderOwner` for brush size controls.

### Outgoing
- **WorldHeightMapEdit**: Calls into this class to apply texture changes (`updateTextures`).
- **OptionsPanel**: Inherits from `COptionsPanel`, suggesting integration with WorldBuilder's options panel system.
- **Tree view controls**: Manages `CTreeCtrl` for terrain category hierarchy display.

## Design Patterns
- **Singleton-like access**: Uses static `m_staticThis` pointer for global access to the dialog instance, common in MFC-based tools.
- **Observer pattern**: Handles notifications via `OnNotify` for dynamic UI updates (e.g., texture swaps).
- **Strategy pattern**: Abstracts brush behavior (texture vs. pathing) via `m_paintingPathingInfo` and `m_paintingPassable` flags.
