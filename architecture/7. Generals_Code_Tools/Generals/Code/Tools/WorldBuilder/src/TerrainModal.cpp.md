# Generals/Code/Tools/WorldBuilder/src/TerrainModal.cpp

## Purpose
Handles terrain texture selection in WorldBuilder, a level editing tool for Generals/Zero Hour.

## Responsibilities
- Manages a dialog for selecting terrain textures
- Populates a tree view with available terrain types
- Updates UI labels and swatches based on selection
- Handles tree view notifications for selection changes

## Key Types
- **TerrainModal (Class)**: Dialog class for terrain texture selection
- **TerrainType (Class)**: Represents terrain types (external)
- **TheTerrainTypes (Global)**: Terrain type registry (external)

## Key Functions
### updateLabel
- Purpose: Updates the terrain name label with the current selection
- Calls: `GetActiveDoc`, `getTexClassUiName`, `SetWindowText`

### OnInitDialog
- Purpose: Initializes the dialog controls and tree view
- Calls: `Create`, `ShowWindow`, `SetWindowText`, `updateTextures`, `setFgTexClass`

### addTerrain
- Purpose: Adds terrain entries to the tree view, organizing them by class
- Calls: `findTerrain`, `findOrAdd`, `InsertItem`

### updateTextures
- Purpose: Refreshes the tree view with current terrain textures
- Calls: `DeleteAllItems`, `isTexClassUsed`, `getTexClassName`, `addTerrain`, `setTerrainTreeViewSelection`

### OnNotify
- Purpose: Handles tree view selection changes
- Calls: `GetSelectedItem`, `GetItem`, `setFgTexClass`, `updateLabel`, `Invalidate`

## Globals
- **m_pathToReplace (AsciiString)**: Path to replace in the terrain selection
- **m_map (WorldHeightMapEdit*)**: Pointer to the height map editor
- **m_currentFgTexture (Int)**: Currently selected foreground texture index

## Dependencies
- **MFC classes**: `CDialog`, `CWnd`, `TVINSERTSTRUCT`, `NMTREEVIEW`
- **External headers**: `TerrainModal.h`, `terrainmaterial.h`, `WHeightMapEdit.h`, `WorldBuilderDoc.h`, `Common/TerrainTypes.h`
- **External symbols**: `TheTerrainTypes`, `TerrainMaterial::setFgTexClass`, `WorldHeightMapEdit::getTexClassName`, `WorldHeightMapEdit::getNumTexClasses`, `WorldHeightMapEdit::isTexClassUsed`, `CWorldBuilderDoc::GetActiveDoc`
