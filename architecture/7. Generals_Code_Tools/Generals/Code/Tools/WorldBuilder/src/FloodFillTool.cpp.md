# Generals/Code/Tools/WorldBuilder/src/FloodFillTool.cpp

## Purpose
Implements a texture tiling tool for the WorldBuilder editor, allowing flood-fill operations on terrain textures.

## Responsibilities
- Handles flood-fill texture application on terrain
- Manages cliff texture adjustments
- Integrates with the undo/redo system
- Controls cursor display based on tool state
- Interfaces with terrain material selection UI

## Key Types
- **FloodFillTool (Class)**: Main tool class for flood-fill operations
- **None**: No additional structs/enums defined

## Key Functions
### `activate()`
- Purpose: Shows terrain material options panel and configures tool state
- Calls: `CMainFrame::GetMainFrame()`, `showOptionsDialog`, `TerrainMaterial::setToolOptions`, `DrawObject::setDoBrushFeedback`

### `setCursor()`
- Purpose: Sets cursor based on whether cliff textures are being adjusted
- Calls: `AfxGetApp()->LoadCursor`, `::SetCursor`, `Tool::setCursor`

### `mouseUp()`
- Purpose: Handles left/right mouse click to perform flood-fill or cliff adjustment
- Calls: `pView->viewToDocCoords`, `pDoc->getCellIndexFromCoord`, `TerrainMaterial::getFgTexClass`, `TerrainMaterial::getBgTexClass`, `htMapEditCopy->doCliffAdjustment`, `htMapEditCopy->floodFill`, `htMapEditCopy->optimizeTiles`, `pDoc->updateHeightMap`, `new WBDocUndoable`, `pDoc->AddAndDoUndoable`

## Globals
- **m_adjustCliffTextures (Bool)**: Tracks whether cliff textures are being adjusted

## Dependencies
- Key includes: `StdAfx.h`, `resource.h`, `FloodFillTool.h
