# Generals/Code/Tools/WorldBuilder/include/BlendMaterial.h

## Purpose
Header for the BlendMaterial dialog class used in WorldBuilder for terrain texture blending.

## Responsibilities
- Manages terrain texture blending UI
- Handles tree view for terrain selection
- Updates blend textures dynamically
- Provides accessors for blend texture class

## Key Types
- **BlendMaterial (Class)**: Dialog for terrain texture blending.
- **WorldHeightMapEdit (Class)**: Forward declaration (external dependency).
- **(anonymous enum)**: Dialog resource ID.
- **IDD (Enum)**: Dialog resource identifier.
- **(anonymous enum)**: Tile size constants (MIN_TILE_SIZE, MAX_TILE_SIZE).

## Key Functions
### BlendMaterial::updateTextures
- Purpose: Updates displayed blend textures.
- Calls: Not inferable.

### BlendMaterial::addTerrain
- Purpose: Adds terrain entry to the tree view.
- Calls: Not inferable.

### BlendMaterial::findOrAdd
- Purpose: Finds or adds a tree view item.
- Calls: Not inferable.

### BlendMaterial::setBlendTexClass
- Purpose: Sets the current blend texture class.
- Calls: Not inferable.

### BlendMaterial::setTerrainTreeViewSelection
- Purpose: Sets the selected terrain in the tree view.
- Calls: Not inferable.

## Globals
- **m_staticThis (BlendMaterial*)**: Static instance pointer.
- **m_updating (Bool)**: Flag for UI update state.
- **m_currentBlendTexture (Int)**: Current blend texture index.

## Dependencies
- `WBPopupSlider.h`, `TerrainSwatches.h`, `OptionsPanel.h`
- `CWnd`, `COptionsPanel`, `CTreeCtrl` (MFC)
- `WorldHeightMapEdit` (forward-declared)
