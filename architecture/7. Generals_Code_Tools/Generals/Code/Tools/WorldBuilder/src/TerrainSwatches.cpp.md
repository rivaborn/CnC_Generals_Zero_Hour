# Generals/Code/Tools/WorldBuilder/src/TerrainSwatches.cpp

## Purpose
Handles rendering of terrain material swatches in the WorldBuilder tool.

## Responsibilities
- Renders background and foreground terrain texture swatches
- Manages message handling for the swatch display window
- Retrieves terrain texture data from the heightmap editor
- Draws texture previews using Windows GDI

## Key Types
- **TerrainSwatches (Class)**: Main window class for displaying terrain swatches
- **BITMAPINFO (Struct)**: Used for texture rendering (external)

## Key Functions
### OnPaint()
- Purpose: Handles the painting of terrain swatches in the window
- Calls: `GetClientRect`, `DrawMyTexture`, `WorldHeightMapEdit::getPointerToClassTileData`, `TerrainMaterial::getFgTexClass`, `TerrainMaterial::getBgTexClass`

### DrawMyTexture()
- Purpose: Renders a texture using Windows GDI StretchDIBits
- Calls: `new BITMAPINFO`, `::StretchDIBits`, `delete`

## Globals
- **SWATCH_OFFSET (const int)**: Offset value for swatch positioning (20)

## Dependencies
- `stdafx.h`, `resource.h`, `TerrainSwatches.h`, `TerrainMaterial.h`, `WorldBuilderDoc.h`, `WHeightMapEdit.h`
- MFC classes: `CWnd`, `CPaintDC`, `CRect`, `CBrush`, `CDC`
- Windows GDI functions: `::StretchDIBits`
- External symbols: `TILE_PIXEL_EXTENT`, `UnsignedByte`, `Int`
