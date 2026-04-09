# Generals/Code/Tools/WorldBuilder/include/TerrainModal.h - Enhanced Analysis

## Architectural Role
This header defines the `TerrainModal` class, a MFC-based dialog for terrain texture editing in WorldBuilder. It bridges the UI layer with the terrain editing core (`WorldHeightMapEdit`), enabling artists to modify terrain textures interactively.

## Cross-References
### Incoming
- Likely called by WorldBuilder's main UI framework when terrain editing is initiated
- Depends on `TerrainSwatches` for texture preview rendering

### Outgoing
- Directly manipulates `WorldHeightMapEdit` for terrain modifications
- Uses MFC's `CDialog` and `CTreeCtrl` for UI implementation

## Design Patterns
- **MVC (Model-View-Controller)**: Separates terrain data (`WorldHeightMapEdit`) from UI controls (`CTreeCtrl`, `TerrainSwatches`)
- **Composite**: Tree view structure organizes terrain textures hierarchically
- **Observer**: Dialog reacts to UI events via `OnNotify()` for dynamic updates

*Not inferable*: No clear use of Factory, Strategy, or Visitor patterns.
