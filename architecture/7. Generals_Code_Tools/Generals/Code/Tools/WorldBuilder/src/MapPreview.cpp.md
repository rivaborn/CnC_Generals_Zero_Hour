# Generals/Code/Tools/WorldBuilder/src/MapPreview.cpp

## Purpose
Generates and saves a preview image (TGA format) of a map in the WorldBuilder tool.

## Responsibilities
- Creates a colorized heightmap preview of the terrain
- Handles water/land color interpolation based on elevation
- Converts map coordinates to world coordinates for sampling
- Saves the preview as a TGA file

## Key Types
- **MapPreview (Class)**: Main class handling preview generation
- **RGBColor (Struct)**: Holds RGB color components (0.0-1.0 range)
- **ICoord2D (Struct)**: 2D integer coordinate
- **Coord3D (Struct)**: 3D coordinate

## Key Functions
### `localIsUnderwater`
- Purpose: Determines if a given coordinate is underwater (not implemented in visible code)
- Calls: None

### `interpolateColorForHeight`
- Purpose: Adjusts color brightness based on terrain height relative to min/max/average heights
- Calls: None

### `mapPreviewToWorld`
- Purpose: Converts preview coordinates to world coordinates
- Calls: `CWorldBuilderDoc::GetActiveDoc()`, `WorldHeightMapEdit::getXExtent()`, `WorldHeightMapEdit::getYExtent()`, `WorldHeightMapEdit::getBorderSize()`

### `buildMapPreviewTexture`
- Purpose: Generates the full preview image by sampling terrain and water colors
- Calls: `localIsUnderwater`, `interpolateColorForHeight`, `mapPreviewToWorld`, `WorldHeightMapEdit::getBoundary()`, `WorldHeightMapEdit::getHeight()`, `WorldHeightMapEdit::getTerrainColorAt()`, `Targa::Save()`

## Globals
- **m_pixelBuffer (UInt32[MAP_PREVIEW_HEIGHT][MAP_PREVIEW_WIDTH])**: Stores the generated preview image pixels

## Dependencies
- `StdAfx.h`, `resource.h`, `WHeightMapEdit.h`, `WorldBuilderDoc.h`, `MapPreview.h`
- `W3DDevice/GameClient/HeightMap.h`, `Common/MapReaderWriterInfo.h`, `Common/FileSystem.h`
- `WWLib/Targa.h`, `common/DataChunk.h`
- `CWorldBuilderDoc`, `WorldHeightMapEdit`, `Targa` classes
- `ICoord2D`, `Coord3D`, `RGBColor` structs
- `MAP_PREVIEW_WIDTH`, `MAP_PREVIEW_HEIGHT`, `MAP_XY_FACTOR` constants
