# Generals/Code/Tools/WorldBuilder/include/TerrainMaterial.h

## Purpose
Header for the TerrainMaterial dialog class used in WorldBuilder for terrain editing.

## Responsibilities
- Manages terrain material selection and painting options
- Handles texture swapping and passability settings
- Provides UI for adjusting brush size and terrain properties
- Integrates with the terrain tree view and swatches display

## Key Types
- **TerrainMaterial (Class)**: Main dialog class for terrain material editing
- **WorldHeightMapEdit (Class)**: Reference to the height map editor (external)
- **(anonymous enum)**: Contains IDD_TERRAIN_MATERIAL dialog ID
- **(anonymous enum)**: Contains MIN_TILE_SIZE and MAX_TILE_SIZE constants

## Key Functions
### DoDataExchange
- Purpose: Handles data exchange between dialog controls and member variables
- Calls: CDataExchange methods

### OnInitDialog
- Purpose: Initializes the dialog and its controls
- Calls: Not inferable

### updateTextures
- Purpose: Updates the terrain textures in the height map editor
- Calls: WorldHeightMapEdit methods

### setToolOptions
- Purpose: Configures tool options based on single cell mode
- Calls: Not inferable

### GetPopSliderInfo/PopSliderChanged/PopSliderFinished
- Purpose: Handles popup slider behavior for brush size adjustment
- Calls: Not inferable

## Globals
- **m_staticThis (TerrainMaterial*)**: Static pointer to the dialog instance
- **m_currentFgTexture (Int)**: Currently selected foreground texture
- **m_currentBgTexture (Int)**: Currently selected background texture
- **m_paintingPathingInfo (Bool)**: Flag for pathing info painting mode
- **m_paintingPassable (Bool)**: Flag for passability painting mode

## Dependencies
- WBPopupSlider.h,
