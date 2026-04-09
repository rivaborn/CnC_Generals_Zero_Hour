# Generals/Code/Tools/WorldBuilder/src/TerrainMaterial.cpp

## Purpose
Handles terrain material selection and editing in the WorldBuilder tool.

## Responsibilities
- Manages terrain texture selection (foreground/background)
- Controls brush size for terrain painting
- Handles passability settings for terrain
- Updates UI elements (tree view, swatches, labels)
- Integrates with heightmap editing tools

## Key Types
- **TerrainMaterial (class)**: Main dialog class for terrain material editing
- **TerrainType (external)**: Represents terrain types (used but not defined here)
- **WorldHeightMapEdit (external)**: Heightmap editing interface

## Key Functions
### `setFgTexClass(Int texClass)`
- Purpose: Sets the foreground texture and updates UI
- Calls: `m_terrainSwatches.Invalidate()`, `updateTextureSelection()`

### `updateTextures(WorldHeightMapEdit *pMap)`
- Purpose: Populates the tree view with available textures
- Calls: `addTerrain()`, `updateTextureSelection()`

### `OnNotify(WPARAM wParam, LPARAM lParam, LRESULT* pResult)`
- Purpose: Handles tree view selection changes
- Calls: `updateLabel()`, `m_terrainSwatches.Invalidate()`

## Globals
- **defaultMaterialIndex (Int)**: Stores the default terrain material index
- **m_staticThis (TerrainMaterial*)**: Singleton instance pointer
- **m_currentFgTexture (Int)**: Currently selected foreground texture
- **m_currentBgTexture (Int)**: Currently selected background texture
- **m_paintingPathingInfo (Bool)**: Flag for pathing info display mode
- **m_paintingPassable (Bool)**: Flag for passability editing mode

## Dependencies
- `terrainmaterial.h`, `WHeightMapEdit.h`, `WorldBuilderDoc.h`
- `TileTool.h`, `WBView3D.h`, `Common/TerrainTypes.h`
- `W3DDevice/GameClient/TerrainTex.h`, `W3DDevice/GameClient/HeightMap.h`
- MFC classes (`CDialog`, `CWnd`, etc.)
- External symbols: `TheTerrainTypes`, `TheTerrainRenderObject`
