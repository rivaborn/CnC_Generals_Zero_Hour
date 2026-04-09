# Generals/Code/Tools/WorldBuilder/src/TerrainModal.cpp - Enhanced Analysis

## Architectural Role
This file implements the terrain texture selection UI in WorldBuilder, bridging the gap between the editor's terrain system and the MFC-based dialog framework. It handles the dynamic population and interaction of terrain types in a hierarchical tree view, reflecting the game's terrain classification system.

## Cross-References
### Incoming
- **WorldBuilderDoc.h**: Uses `CWorldBuilderDoc::GetActiveDoc()` to access the active document's height map
- **WHeightMapEdit.h**: Relies on `WorldHeightMapEdit` methods for texture class management
- **Common/TerrainTypes.h**: Uses `TheTerrainTypes` global for terrain type lookups

### Outgoing
- **terrainmaterial.h**: Calls `TerrainMaterial::setFgTexClass()` to update the active terrain material
- **MFC framework**: Uses `CDialog`, `CWnd`, and tree view controls for UI rendering
- **Resource system**: References dialog resources (IDD, IDC_*) defined in .rc files

## Design Patterns
- **Composite Pattern**: The tree view structure organizes terrain types hierarchically (by class/legacy status), allowing recursive traversal in `setTerrainTreeViewSelection`
- **Observer Pattern**: Handles `TVN_SELCHANGED` notifications to update the UI state when selections change
- **Strategy Pattern**: The terrain classification logic in `addTerrain` dynamically routes entries based on whether they're INI-defined or legacy GDF entries

*Not inferable*: No clear use of Factory, Decorator, or Visitor patterns in this file.
