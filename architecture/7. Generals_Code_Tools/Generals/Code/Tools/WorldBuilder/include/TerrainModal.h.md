# Generals/Code/Tools/WorldBuilder/include/TerrainModal.h

## Purpose
Header file for the TerrainModal dialog class used in the WorldBuilder tool for terrain editing.

## Responsibilities
- Manages terrain texture selection and editing
- Handles tree view UI for terrain categories
- Updates terrain swatches and labels
- Interfaces with WorldHeightMapEdit for terrain modifications

## Key Types
- **TerrainModal (Class)**: Dialog for terrain editing in WorldBuilder.
- **WorldHeightMapEdit (Class)**: Reference to the height map editor (external).
- **(anonymous enum) (Enum)**: Contains IDD_TERRAIN_MODAL dialog identifier.
- **IDD (Enum)**: Dialog resource ID.

## Key Functions
### TerrainModal()
- Purpose: Constructor for TerrainModal dialog.
- Calls: None visible.

### DoDataExchange()
- Purpose: Handles data exchange between dialog controls and member variables.
- Calls: None visible.

### OnNotify()
- Purpose: Processes notification messages from dialog controls.
- Calls: None visible.

### OnInitDialog()
- Purpose: Initializes the dialog when created.
- Calls: None visible.

### addTerrain()
- Purpose: Adds a terrain entry to the tree view.
- Calls: findOrAdd().

### findOrAdd()
- Purpose: Finds or adds a tree node for a given label.
- Calls: None visible.

### updateLabel()
- Purpose: Updates the label for the current terrain selection.
- Calls: None visible.

### updateTextures()
- Purpose: Updates the terrain texture swatches.
- Calls: None visible.

### setTerrainTreeViewSelection()
- Purpose: Sets the selection in the terrain tree view.
- Calls: None visible.

### getNewNdx()
- Purpose: Returns the current foreground texture index.
- Calls: None visible.

## Globals
- **m_current
