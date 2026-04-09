# Generals/Code/Tools/WorldBuilder/include/BuildList.h - Enhanced Analysis

## Architectural Role
This header defines the `BuildList` class, a key component of WorldBuilder's UI layer for managing building placement and properties. It bridges the gap between the editor's terrain manipulation tools and the game's building system, allowing level designers to configure building lists per faction.

## Cross-References
### Incoming
- Likely called by `WorldBuilder`'s main UI framework (e.g., `MainFrm` or `WorldBuilderDoc`) to display the building list panel.
- `BuildListInfo` instances are probably created/modified by other WorldBuilder tools (e.g., `BuildingPlacer`).

### Outgoing
- Depends on `TerrainSwatches` for terrain-related UI elements.
- Uses `OptionsPanel` (MFC-based) for dialog management.
- Interacts with `WBPopupSlider` for height/angle adjustments.
- Calls into `WorldHeightMapEdit` for terrain modifications (inferred from `m_heightSlider`).

## Design Patterns
- **Singleton-like access**: Uses `m_staticThis` for global access to the dialog instance, though not a strict singleton.
- **Observer pattern**: `update()` method suggests this class observes changes in building lists (e.g., faction selection).
- **Command pattern**: `addBuilding()` likely encapsulates building placement logic for undo/redo (common in editors).

*Not inferable*: No clear use of Factory, Strategy, or Visitor patterns.
